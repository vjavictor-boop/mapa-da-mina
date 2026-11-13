# Mapa da Mina

Lugares disponíveis em fretamentos e bloqueios aéreos, por rota e mês de embarque.

- `index.html`: o site (filtros, mapa de calor rota × mês, ranking de rotas, destinos e voos com mais lugares livres).
- `voos.csv`: um voo por linha, exportado do Power BI "Disponibilidade Fretamento" (página Tabela_Exportação), com dados até 13/11/2026.

## Como atualizar

1. No Power BI, exporte de novo a página Tabela_Exportação.
2. Gere um novo `voos.csv` com as mesmas colunas: `data,mes,origem,destino,rota,itinerario,cia,tipo,oferta,confirmado,reservado,disponivel,retorno`.
3. Substitua o arquivo `voos.csv` no repositório. O site se atualiza sozinho.

## Histórico de preços

- `precos.csv`: menor preço por semana de embarque, por destino, em cada coleta. Colunas: `coleta,origem,iata,destino,semana,data,preco,promo`. O preço é por pessoa, com taxas, para 2 adultos, tirado do calendário "a partir de" do Atlas (Pacote exclusivo).
- `amostras.csv`: um orçamento por destino e coleta, na saída mais barata, com o valor final, o link do Atlas e o print.
- `prints/AAAA-MM-DD/`: prints dos orçamentos, com o cabeçalho do Atlas cortado.

Para uma nova coleta, acrescente linhas com a nova data em `coleta` nos dois arquivos e crie a pasta de prints do dia. Coletas antigas não são apagadas, e é isso que forma o histórico.

## Indicadores

- **Oferta**: lugares bloqueados no voo.
- **Ocupados**: confirmados + reservados.
- **Ocupação**: ocupados ÷ oferta.
- **Disponível**: oferta − ocupados.

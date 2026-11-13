# Mapa da Mina

Lugares disponíveis em fretamentos e bloqueios aéreos, por rota e mês de embarque.

- `index.html`: o site (filtros, mapa de calor rota × mês, ranking de rotas, destinos e voos com mais lugares livres).
- `voos.csv`: um voo por linha, exportado do Power BI "Disponibilidade Fretamento" (página Tabela_Exportação), com dados até 13/11/2026.

## Como atualizar

1. No Power BI, exporte de novo a página Tabela_Exportação.
2. Gere um novo `voos.csv` com as mesmas colunas: `data,mes,origem,destino,rota,itinerario,cia,tipo,oferta,confirmado,reservado,disponivel,retorno`.
3. Substitua o arquivo `voos.csv` no repositório. O site se atualiza sozinho.

## Indicadores

- **Oferta**: lugares bloqueados no voo.
- **Ocupados**: confirmados + reservados.
- **Ocupação**: ocupados ÷ oferta.
- **Disponível**: oferta − ocupados.

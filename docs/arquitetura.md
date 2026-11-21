# Arquitetura e Fluxo do MVP — ClimaFix

## Stack Utilizada
- **Frontend:** React + TypeScript + Tailwind CSS + Shadcn/UI (gerado via Lovable)
- **Backend & Auth:** Lovable Cloud (Banco de dados relacional e autenticação administrativa)
- **Integração Comercial:** Deep Link dinâmico (`wa.me`) com payload codificado via `encodeURIComponent`

## Estrutura de Dados (Lovable Cloud)
1. **`leads`**: Armazena simulações enviadas pela Landing Page (`nome`, `empresa`, `tipo_ambiente`, `equipamentos`, `frequencia`, `valor_estimado`, `status`).
2. **`clients`**: Clientes convertidos a partir dos leads com cálculo de ciclo preventivo (`30`, `60` ou `90` dias) e observações técnicas.
3. **`appointments`**: Agenda de visitas preventivas vinculada aos clientes ativos.

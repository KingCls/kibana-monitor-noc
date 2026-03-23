# Kibana Monitor NOC

Monitor local para acompanhar consultas do Kibana e destacar novos erros em um dashboard web.

## Requisitos

- Python 3.10+
- Acesso ao Kibana monitorado

## Arquivos principais

- `monitor.py`: servidor HTTP e loop de monitoramento
- `dashboard.html`: interface web local
- `config.example.json`: modelo de configuracao

## Configuracao

1. Crie um arquivo `config.json` na mesma pasta com base em `config.example.json`.
2. Preencha `kibana_url`, `usuario`, `senha` e a lista `links`.
3. Ajuste `intervalo_minutos` e `porta_dashboard` se necessario.

## Como executar

```bash
python3 monitor.py
```

O monitor inicia o servidor local e tenta abrir o dashboard automaticamente.

## Seguranca

- `config.json` fica fora do versionamento e deve conter as credenciais locais.
- Pastas de execucao como `logs/`, `cache/`, `historico/` e `__pycache__/` nao sao publicadas.

## Publicacao

Repositorio remoto:

- `https://github.com/KingCls/kibana-monitor-noc`
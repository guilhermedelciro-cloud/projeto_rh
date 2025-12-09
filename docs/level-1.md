---
config:
  layout: dagre
---
flowchart TB
    Cliente["Colaborador"] -- Registra ponto eletrônico e consulta documentos/holerites --> Sistema["RH Management"]
    Atendente["Analista de RH"] -- "Gerencia e configura dados (Cadastro, Ponto, Folha)." --> Sistema
    Tecnico@{ label: "<span data-path-to-node=\"9,3,0,0\"><b>Gestor/Empresário</b></span>" } -- "Visualiza dashboards gerenciais e relatórios de desempenho." --> Sistema
    Sistema -- "Envia arquivos (layout CNAB) com dados para processamento de pagamentos da folha." --> Email["Sistema Bancário"]
    Sistema -- "Exporta dados obrigatórios para conformidade legal e recolhimento de encargos." --> n1["eSocial / Órgãos Gov"]

    Tecnico@{ shape: rect}

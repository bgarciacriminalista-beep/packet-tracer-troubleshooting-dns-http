
🌐 Cisco Networking Lab: End-to-End Connectivity & Service Implementation
Este repositório documenta a implementação prática de uma infraestrutura de rede segmentada, realizada através do Cisco Packet Tracer. O projeto foca na configuração de serviços essenciais, roteamento entre sub-redes e análise profunda do fluxo de dados no Modelo OSI.

🎯 Objetivos do Projeto
Estabelecer conectividade entre duas sub-redes distintas via roteador.
Implementar e validar serviços de Camada de Aplicação (HTTP e DNS).
Analisar o comportamento do protocolo TCP durante o estabelecimento de conexão.
Aplicar técnicas de troubleshooting para resolver falhas de endereçamento e resolução de nomes.

🛠️ Tecnologias e Protocolos
Simulação: Cisco Packet Tracer
Camada de Aplicação: HTTP, DNS
Camada de Transporte: TCP (Aperto de Mão Tripartido)
Camada de Rede: IPv4, ICMP, Roteamento (Gateway)
Ferramentas de Diagnóstico: Ping, Ipconfig, NSLookup, PDUs do Modo Simulação.

🚀 Passo a Passo da Implementação
1. Infraestrutura Lógica
Configurei as interfaces do roteador para servirem como Default Gateways das redes e , garantindo que os hosts pudessem sair de suas redes locais.192.168.1.0/2410.0.0.0/24

2. Configuração de Serviços
No Servidor Web, estabeleci:

Serviço HTTP: Edição do arquivo para personalização da interface.index.html
Serviço DNS: Criação de um registro do tipo A (Address Record) mapeando o domínio para o IP .ciscolearn.web.com10.0.0.10

3. Análise de Simulação (PDU Complexa)
Utilizei o modo de simulação para observar o encapsulamento. Verifiquei o tráfego periódico configurado com:
Fonte Porta: 1000
Porto de destino: 80 (HTTP)
Protocolo de Transporte: TCP

🔍 Solução de problemas (Onde o aprendizado acontece!)
Durante o laboratório, identifiquei e corrigi os seguintes desafios:
Máscara de Sub-rede: Correção de endereçamentos incompletos que impediam a comunicação local.
Resolução DNS: Diagnóstico do erro "Couldnt find host", resolvido através da ativação do serviço DNS e apontamento correto do DNS Server no host cliente.
Portal Perdido: Garantia de que todos os dispositivos conheciam sua porta de saída para permitir o tráfego inter-redes.

🛡️ Conexão com Cibersegurança e Perícia Forense
Este exercício fornece a base crítica para profissionais de segurança:
Defesa: O entendimento do TCP Handshake é vital para mitigar ataques de SYN Flood.
Monitoramento: A análise de DNS auxilia na identificação de ataques de DNS Spoofing ou redirecionamentos maliciosos.
Forense: A capacidade de rastrear um pacote do IP de origem ao destino, analisando cada salto (hop) e camada OSI, é a técnica fundamental para investigar exfiltração de dados e intrusões.

📂 Como visualizar este projeto
Baixe o arquivo presente neste repositório..pkt
Abra no Cisco Packet Tracer (v8.0 ou superior).
Use o Web Browser do PC Cliente para acessar .ciscolearn.web.com

Desenvolvido por Bruno Garcia - Estudante de Redes e Cibersegurança.

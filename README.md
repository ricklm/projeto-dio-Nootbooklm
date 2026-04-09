# 🛡️ Guia Tático de Cibersegurança: Red & Blue Team com NotebookLM

Este repositório apresenta um projeto prático desenvolvido para o desafio de IA da DIO. O objetivo é utilizar o **NotebookLM** para processar e organizar o conhecimento contido nos principais manuais de campo da cibersegurança moderna, focando em **OSINT** e operações híbridas.

## 🎯 Contexto e Objetivos

Como profissional de engenharia de software em ambiente bancário, a segurança não é apenas um requisito, é a fundação do código. Este caderno temático foi criado para consolidar técnicas de ataque e defesa, permitindo uma resposta rápida a incidentes e uma coleta de dados estratégica através de fontes abertas.

**Objetivos de Estudo:**
1. Mapear vulnerabilidades críticas em infraestruturas Windows e Linux[cite: .
2. Dominar técnicas de **OSINT** para reconhecimento passivo e inteligência de dados.
3. Consolidar uma base de comandos "ready-to-use" para testes de penetração e auditoria.

## 📚 Curadoria de Fontes "Field Manual"

Para este projeto, utilizei os três pilares da literatura tática de cibersegurança:

1. **RTFM v2.0 (Red Team Field Manual):** Manual técnico atualizado em 2022, focado em comandos ofensivos para sistemas modernos como Windows Server 2022 e Kali Linux 2022.2.
2. **BTFM (Blue Team Field Manual):** Guia tático focado em defesa, resposta a incidentes e análise forense de rede.
3. **The Operator Handbook (v1.0):** Referência técnica massiva que integra Red Team, Blue Team e uma seção profunda sobre ferramentas de OSINT.

---

## 🧠 Engenharia de Prompts e Cicatrizes (Troubleshooting)

Neste projeto, a IA foi utilizada como uma ferramenta de **curadoria inteligente**. Documento abaixo os testes realizados no NotebookLM:

### Teste 1: Consolidação de OSINT
* **Prompt Estratégico:** *"Com base nos manuais carregados, crie uma tabela consolidada de recursos de OSINT, separando-os por categoria (Busca de Pessoas, Reconhecimento de Rede e Ferramentas de Relacionamento)."*
* **Resultado:** Categoria
Ferramenta
Descrição / Uso
Busca de Pessoas
Fast People Search / True People Search
Focadas na pesquisa de dados pessoais e pesquisa reversa de endereços (fastpeoplesearch.com, truepeoplesearch.com)
.
White Pages
Diretório online para buscar endereços e pessoas (whitepages.com)
.
Intelius / Radaris / Nuwber
Mecanismos de busca de registros, histórico e informações de indivíduos (intelius.com, radaris.com, nuwber.com)
.
Spytox / That's Them
Busca de dados e correlação de pessoas, emails e telefones (spytox.com, thatsthem.com)
.
Dehashed
Ferramenta voltada à pesquisa de emails, telefones e identificação de dados vazados/comprometidos (dehashed.com)
.
True Caller / Sly Dial
Identificação e busca em bases de números de telefone e operadoras de telefonia (truecaller.com, slydial.com)
.
Name Checkr / KnowEm
Usadas para procurar ou verificar a disponibilidade e uso de nomes de usuário (usernames) em múltiplas plataformas
.
Reconhecimento de Rede
Shodan
Motor de busca especializado para identificar dispositivos conectados à Internet, visualizar IPs, portas, sistemas operacionais e faixas de rede (shodan.io)
.
Censys
Auxilia no reconhecimento de IPv4, pesquisa de infraestruturas conectadas e transparência de certificados (censys.io)
.
Nmap
Scanner de rede utilizado para realizar a varredura e descoberta de hosts, portas abertas e enumeração de serviços (HTTP, DNS, etc.)
.
DNS Dumpster / DNS Trails
Mapeamento e enumeração de subdomínios, registros DNS e histórico de infraestrutura (dnsdumpster.com, dnstrails.com)
.
ViewDNS / Whoxy / Whoisology
Conjunto de ferramentas para varredura de portas, pesquisas WHOIS e engenharia reversa de IPs e domínios (viewdns.info, whoxy.com)
.
Built With
Realiza o perfilamento identificando as tecnologias e os componentes instalados em sites/infraestrutura (builtwith.com)
.
Wigle
Plataforma voltada para mapeamento global e reconhecimento focado em redes sem fio/Wi-Fi (wigle.net)
.
Threat Crowd / Virus Total
Plataformas para o levantamento de inteligência de ameaças vinculadas a IPs, domínios e infraestruturas (threatcrowd.org, virustotal.com)
.
Ferramentas de Relacionamento
Skopenow
Ferramenta ampla de investigações em mídias sociais para analisar relacionamentos a partir de nomes, telefones, emails e usernames (skopenow.com)
.
Social Searcher
Mecanismo de busca e monitoramento focado especificamente em analisar perfis e atividades conjuntas em diversas redes sociais (social-searcher.com)
.
Socilab
Utilizada para visualização e análise profunda da rede de relacionamentos e conexões profissionais do próprio usuário no LinkedIn (socilab.com)
.
StalkScan / Graph.tips
Realizam buscas gráficas e pesquisas avançadas automáticas em perfis e conexões no Facebook (stalkscan.com, graph.tips/beta)
.
Gramfly
Permite visualizar as atividades e conexões de interação dos usuários na rede social Instagram (gramfly.com)
.
Treeverse
Extensão de navegador usada para visualizar as conexões e a ramificação de conversas e discussões no Twitter
.
Twint / Twlets
Ferramentas (como a raspagem em Python do Twint) para coletar as relações de um perfil no Twitter: seguidores, contas que segue, curtidas e tweets, burlando limites de API
.
F5Bot
Monitora relacionamentos de tópicos ou envia alertas de e-mail sobre palavras-chave ou entidades mencionadas na rede Reddit
obs:identifiquei que o Facebook mudou sua API e o StalkScan original não funciona mais como antes, no contexto de 2026, pesquisadores de OSINT agora utilizam mais o Graph.tips ou técnicas manuais de busca avançada para obter os mesmos resultados.

### Teste 2: Identificação de Portas e Protocolos
* **Prompt Refinado:** *"Aja como um auditor de segurança. Liste as 10 portas mais críticas para um ambiente bancário e os respectivos serviços, citando o manual de referência."*
* **Resultado:Como auditor de segurança, e baseando-me nos manuais de referência de táticas defensivas e ofensivas (como o Operator Handbook e o Blue Team Field Manual), avalio que a superfície de ataque em um ambiente bancário deve ser minimizada ao máximo. Instituições financeiras lidam com dados altamente sensíveis (informações de clientes, transações e segredos corporativos) e são alvos constantes de ataques cibernéticos.
Abaixo, listo as 10 portas mais críticas (e seus respectivos serviços) que devem ser rigorosamente monitoradas, filtradas ou bloqueadas em um ambiente bancário, citando o manual de referência:
1. Portas 139 e 445 (TCP/UDP) - SMB e NetBIOS
Serviço: Server Message Block / NetBIOS Session Service
.
Risco no Banco: Extremamente críticas. São usadas para compartilhamento de arquivos e impressoras em redes Windows
. Quando expostas ou mal configuradas, são o principal vetor para movimentação lateral de invasores e rápida propagação de malwares catastróficos, como ransomwares (ex: WannaCry), podendo paralisar as operações da agência bancária
.
2. Porta 1433 (TCP/UDP) - MS-SQL
Serviço: Microsoft SQL Server
.
Risco no Banco: Bancos de dados são o "cofre" digital da instituição, armazenando dados de cartões, saldos e históricos financeiros. A exposição dessa porta para redes não confiáveis permite ataques de força bruta, injeção de SQL ou exploração de vulnerabilidades para exfiltração de dados
.
3. Porta 3389 (TCP) - RDP
Serviço: Remote Desktop Protocol / Terminal Services
.
Risco no Banco: Permite acesso à área de trabalho remota de servidores e estações de trabalho
. É um dos vetores de ataque mais comuns para invasores tentarem acesso não autorizado por meio de força bruta ou credenciais vazadas. Jamais deve estar exposta diretamente à internet.
4. Porta 22 (TCP) - SSH
Serviço: Secure Shell
.
Risco no Banco: Usada primariamente para administração remota segura de servidores Linux e dispositivos de rede
. Embora criptografada, se a porta for exposta e a autenticação baseada em senha estiver ativa (em vez de chaves públicas), a infraestrutura core do banco fica vulnerável a ataques de força bruta e acesso de administradores não autorizados.
5. Portas 21 (TCP) e 23 (TCP) - FTP e Telnet
Serviço: File Transfer Protocol e Telnet
.
Risco no Banco: São protocolos legados que trafegam dados (incluindo senhas e arquivos corporativos) em texto claro (sem criptografia)
. A presença desses serviços em um banco viola gravemente normas de conformidade (como PCI-DSS e Bacen), pois permite interceptação fácil (sniffing) na rede.
6. Porta 3306 (TCP) - MySQL / MariaDB
Serviço: Banco de dados MySQL
.
Risco no Banco: Similar ao MS-SQL, o MySQL é amplamente utilizado em aplicações web e intranets corporativas. Sua exposição indevida pode levar ao roubo completo ou à corrupção da base de dados de serviços da instituição financeira
.
7. Portas 389 e 636 (TCP/UDP) - LDAP e LDAPS
Serviço: Lightweight Directory Access Protocol (texto claro e via SSL, respectivamente)
.
Risco no Banco: Serviços de diretório, como o Active Directory (AD)
, são o coração do controle de acessos em uma rede corporativa bancária. Se um invasor alcançar essas portas, poderá enumerar todos os usuários, grupos e permissões da rede, facilitando escalonamento de privilégios
. A porta 389 é ainda mais crítica por não exigir criptografia por padrão.
8. Portas 80 e 443 (TCP) - HTTP e HTTPS
Serviço: World Wide Web / Tráfego de aplicações Web
.
Risco no Banco: Embora o tráfego 443 (HTTPS)
 seja necessário para o Internet Banking e APIs, essas portas são a principal porta de entrada de clientes e, consequentemente, o maior vetor para exploração de vulnerabilidades de aplicações web (Cross-Site Scripting, injeções, etc.). Devem estar estritamente sob a proteção de WAFs (Web Application Firewalls). A porta 80
 (texto claro) deve ser usada estritamente para forçar o redirecionamento para a porta 443.
9. Portas 161 e 162 (UDP) - SNMP
Serviço: Simple Network Management Protocol e SNMP Traps
.
Risco no Banco: Utilizado para gerenciar switches, roteadores e servidores na rede
. Especialmente nas versões 1 e 2c, as requisições de leitura/escrita são trafegadas em texto claro através de "community strings". O comprometimento dessas portas entrega ao invasor a "planta baixa" de todo o ambiente de rede do banco
.
10. Porta 53 (TCP/UDP) - DNS
Serviço: Domain Name System
.
Risco no Banco: Fundamental para a resolução de nomes
, os servidores DNS bancários sofrem constante ameaça de ataques DDoS (negação de serviço), envenenamento de cache (DNS Spoofing - para redirecionar clientes a sites de phishing bancário) e também abuso por malwares para exfiltração de dados restritos através de DNS Tunneling
.
Recomendação de Auditoria: Para garantir a confidencialidade, integridade e disponibilidade do ambiente bancário, deve-se adotar o princípio do privilégio mínimo: fechar todas as portas por padrão (Default Deny) e permitir apenas o tráfego estritamente necessário para operações validadas, sob arquitetura segmentada e rigorosamente monitorada
obs: Notei que a IA sugeriu o monitoramento das portas 21 (FTP) e 23 (Telnet). Como estudante de cibersegurança, identifiquei que esses protocolos trafegam dados em texto claro, o que viola normas fundamentais de segurança bancária.

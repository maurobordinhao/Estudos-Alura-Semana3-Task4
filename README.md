# Estudos-Alura-Semana3-Task4

Funcionalidade: Login

Modelagem de ameaças / Metodologia: STRIDE 

Abaixo serão listados os riscos que uma funcionalidade de Login pode enfrentar e quais são os tipos de atacantes que podem explorar esses riscos

S - (Spoofing) 

- Ex: Uma pessoa criminosa pode tentar se passar por outra pessoa que possui um login válido, utilizando credenciais vazadas, roubadas, ou senhas fracas.

Maneiras de diminuir o problema: 
Utilizar MFA, criar política que obrigue uso senha forte/segura, obrigar a renovação periodica de senhas, etc

T - (Tampeting) 
- Ex: Modificação de dados de forma maliciosa por um hacker durante o processo de autenticação, alterando requisições ou tokens (Headers: chave:valor, scripts).

Maneira de diminuir o problema>  
Uso de assinaturas digitais e certificados seguros, validações de entrada, etc

R - (Repudiation) 
- Ex: O usuário de forma criminosa pode tentar negar ter realizado Login ou uma ação específica e sensível que ele fez, se não tiver logs ou trilhas adequadas.

Maneiras de diminuir o problema: 
Criar logs de acesso com horários e atividades para registro de ações do usuário, auditoria de ações, política de rotação de logs e recuperação, etc

I - Information Disclosure) - Clone da página (Cross Origin), Inspeção de logs, erros detalhados com informações internas ao invés de erros genéricos no terminal.

- Ex: Pode ocorrer vazamento de informações sensíveis, mensagens de erro que revelam detalhes do sistema/linguagens/versões utilizadas, se determinado usuário existe ou não, credenciais expostas. 
Cibercriminosos podem causar essas situações e podem se aproveitar disso.

Maneiras de diminuir o problema: 
Implementar anonimização de dados sensiveis, controlar informações visíveis na url que porventura possam disponibilizar informações internas de infraestrutura de desenvolvimento,
evitar uso de env e usar secrets para credenciais, etc

D - (Denial of Service) 
- Ataques DOS que causam indisponibilidade do login e impedem usuários verdadeiros de acessarem o sistema, como por exemplo, tentativa de força bruta/sobrecarga no login. 
Esses ataques podem ser feitos por criminosos, bots,

Maneiras de diminuir o problema: 
Usar mecanismos que identifiquem ataques DOS/DDOS, firewalls waf que protejam e requeiram testes antes de efetuar o login, uso de captive portal para diminuir uso de bots,
Identificar origem (usuário + ip) de acesso suspeito e realizar bloqueio, etc 

E - (Elevation of privilege) - path indevido, token + header (+perfil), 
- Ex: Exploração de falhas de segurança na autenticação que permitem a um criminoso acessar privilégios administrativos do sistema

Maneiras de diminuir o problema:
Acompanhar divulgação de CVEs e manter atualizadas as soluções de software envolvidas na app de login, usar níveis de acesso e políticas de testes de acesso para subir privilégio de acesso.

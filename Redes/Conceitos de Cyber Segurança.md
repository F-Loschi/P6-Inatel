Nome: Felipe Silva Loschi
Matrícula: 601 - GES
1) O que diferencia um sistema de chaves simétricas de um sistema de chaves assimétricas? Cite uma vantagem e uma desvantagem de cada sistema. Dê exemplos de algoritmos que implementam cada tipo de sistema.
	
	Resposta:  Criptografia simétrica e assimétrica são técnicas que permitem transformar dados em códigos indecifráveis para pessoas  que não possuem a chave correta para decodificá-los. Dessa forma, é preciso proteger informações sensíveis contra acessos não autorizados, garantindo a confidencialidade, a integridade e a autenticidade dos dados. A criptografia simétrica ou criptografia de chave secreta ou compartilhada utiliza uma única chave, que é compartilhada entre o emissor e o receptor da mensagem; já a criptografia assimétrica ou criptografia de chave pública ou de dois fatores utiliza um par de chaves: uma pública e uma privada. A chave pública pode ser divulgada livremente para qualquer pessoa, enquanto a chave privada deve ser mantida em sigilo pelo seu dono.
2) O que é e qual a finalidade de um nonce em um protocolo de autenticação?
	
	Resposta: Nonce é um número aleatório ou pseudoaleatório usado em protocolos de comunicação, um nonce criptográfico ajuda a manter as comunicações privadas. É um número arbitrário e gerado aleatoriamente que só pode ser usado uma vez e, muitas vezes, também inclui um registro de data e hora. Um nonce criptográfico pode ajuda a evitar ataques de repetição, garantindo que comunicações antigas não possam ser reutilizadas por pessoas mal-intencionadas. Os nonces criptográficos são usados em autenticação, protocolos, funções hash criptográficas e vetores de inicialização.
3) O que é uma "Assinatura Digital" e qual a sua função?
	
	Resposta: Uma Assinatura Digital é um esquema matemático para verificar a autenticidade de mensagens ou documentos digitais. Uma assinatura digital válida, ou seja, aquela em que os pré-requisitos são atendidos , dá ao mesmo destinatário uma confiança muito alta de que a mensagem foi criada  por um remetente conhecido (autenticidade) e que a mensagem não foi alterada em trânsito (integridade).
4) O que é um hash (Resumo de Mensagem)? Qual a sua função, no contexto de segurança?
	
	 Reposta: O hashing é uma função matemática unidirecional que transforma dados em uma sequência de texto não descritivo que não pode ser revertida ou decodificada. 
	 No contexto da cibersegurança, o hashing é uma forma de manter informações e dados sensíveis — incluindo senhas, mensagens e documentos — em segurança. Uma vez que esse conteúdo é convertido por meio de um algoritmo de hashing, o valor resultante (ou código hash) torna-se ilegível para humanos e extremamente difícil de decifrar, mesmo com o auxílio de tecnologia avançada.
5) O que é um "Certificado Digital"? Como ele funciona?
	
	Resposta: O certificado digital é a identidade digital da pessoa física e jurídica na internet. E, por isso, por meio dele é possível realizar diversos serviços online, como a entrega de declarações e obrigações e a assinatura de documentos. Tudo que é realizado via certificado digital tem validade jurídica prevista na legislação.
	- e-CPF:
		O e-CPF é a identidade da pessoa física na internet. Ele pode ser usado para enviar declarações e obrigações, acessar sites e serviços e para assinar documentos com validade jurídica.
	- e-CNPJ:
		O e-CNPJ é a identidade de pessoas jurídicas/empresas na internet. Ele pode ser usado para acessar sites, sistemas e serviços e para assinar notas fiscais e outros documentos com validade jurídica.
	- e-CNPJ PME:
		O e-CNPJ PME é a identidade de pequenas e médias empresas na internet. Ele pode ser usado para acessar sites, sistemas e serviços e para assinar notas fiscais e outros documentos com validade jurídica.
	- CT-e:
		O certificado digital CT-e atribui validade jurídica e garante a autenticidade do documento de Conhecimento de Transporte Eletrônico de Cargas. Ele pode ser emitido atrelado ao CNPJ da empresa, mas em nome do funcionário responsável pela emissão do documento ou terceiros que não sejam o representante legal.
	- NF-e:
		O certificado digital NF-e é específico para assinatura de notas fiscais eletrônicas (NF-e). Ele  pode ser emitido atrelado ao CNPJ da empresa, mas em do nome do funcionário responsável pela emissão do documento.
6) Qual o papel de uma "Central de Distribuição de Chaves - KDC"?
	
	Resposta: Uma KDC atua na autenticação de terceiros, assim os usuários comprovam suas identidades a um servidor centralizado, que é chamado de Central de Distribuição de Chaves. Podendo usar então esses ingressos para comprovar sua identidade na rede, eliminando a necessidade de vários signos para diferentes sistemas
7) Qual o papel de uma "Autoridade Certificadora - AC"?
	
	Resposta: Uma Autoridade Certificadora é aquela responsável pelo papel de emitir certificados digitais e assinaturas, essencial para promover a confiabilidade e integridade em largas escalas. Podendo fornecer esses serviços a empresas, websites e indivíduos. A validação feita por elas gera a confiança entre usuários e sites, assim protegendo dados sensíveis como senhas e outras informações pessoais.
- Referências:
	- 1, 2 e 3:
		-  https://pt.wikipedia.org/wiki/Assinatura_digital, https://www.totvs.com/blog/gestao-para-assinatura-de-documentos/criptografia-simetrica-e-assimetrica/
		- https://www.okta.com/identity-101/nonce/
	- 4 e 5: 
		- https://www-crowdstrike-com.translate.goog/en-us/cybersecurity-101/data-protection/data-hashing/?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=sge#:~:text=Hashing%20é%20uma%20função%20matemática,para%20manter%20essas%20informações%20seguras.
		- https://certisign.com.br/tudo-sobre-certificados-digitais#:~:text=O%20que%20é%20o%20certificado,validade%20jurídica%20prevista%20na%20legislação.
	- 6 e 7:
		- https://www.ibm.com/docs/pt-br/i/7.5.0?topic=concepts-network-authentication-service-protocols
		- https://www-digicert-com.translate.goog/blog/what-is-a-certificate-authority?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=tc
		- https://www-sectigo-com.translate.goog/resource-library/what-is-a-certificate-authority?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=tc
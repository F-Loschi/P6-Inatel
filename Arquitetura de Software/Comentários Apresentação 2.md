## Equipe 1

### Tema 7: Gestão de partidas

#### Pontos positivos:
- Refizeram o caso de uso adaptando aos reviews da última apresentação
- Apesar de enxuto, o UML é claro e objetivo
- Souberam explicar quais princípios SOLID aplicavam e justificar por que não aplicavam os outros
- Quebraram uma classe que anteriormente estava sobrecarregada
#### Pontos negativos:
- Apesar de não precisarem ter uma conexão direta com o jogador, pensando na necessidade de login e outras funcionalidades, precisam ter uma entidade que represente o jogador em seu UML
- A agregação da `FilaDeBatalha` não faz sentido no contexto modelado
- A composição de `MatchMaking` não faz sentido
- Precisam de uma classe que comunique com o `ServiçoDeBatalha`; não pode ter o sistema em si diretamente no UML
- Simplificaram demais e não conseguiram aplicar alguns conceitos; poderiam ter complexificado um pouco mais para poder aplicá-los adequadamente
---
## Equipe 2
### Tema 3: Trocas
#### Pontos positivos:
- Refizeram o diagrama de caso de uso
- Houve melhora significativa em relação ao último diagrama
- Comunicaram-se com os outros grupos para alinhamento
#### Pontos negativos:
- Não conseguiram diferenciar classes abstratas de classes concretas adequadamente
- A `PokeAPI` é acessada em todos os lugares, mesmo onde não precisaria ser chamada
- UML confuso devido ao tamanho, que talvez seja desnecessário
- O princípio de Liskov não ficou bem especificado
---
## Equipe 3
### Tema 2: Distribuição de cartas
*Meu grupo*
---
## Equipe 4
### Tema 8: Batalha
#### Pontos positivos:
- Fizeram as devidas alterações para ajustar ao SOLID
- Criação de interfaces que se adaptam perfeitamente aos princípios SOLID
- Melhorias visuais nos diagramas
- Conversaram com os outros grupos e se alinharam
- Conseguiram usar o princípio de Interface Segregation adequadamente
#### Pontos negativos:
- Não aplicam alguns conceitos por dizer que não precisam
- Poderiam ter mais interfaces para melhor segregação
- Algumas setas estavam no sentido errado no diagrama de caso de uso
- Faltaram atores importantes, como: Sistema de Distribuição de Cartas, PokeAPI, Login
---
## Equipe 5
### Tema 6: Painel de administração
#### Pontos positivos:
- Atualizaram alguns `<<include>>` para `<<extend>>`
- Removeram a relação incorreta do administrador com os outros agentes
#### Pontos negativos:
- Falta de controllers no diagrama
---
## Equipe 6
### Tema 5: Visualização de trocas
#### Pontos positivos:
- Mudaram todas as relações do diagrama
- Anteriormente feriam o princípio S (Single Responsibility); agora segregaram em várias classes para respeitá-lo
- Destrincharam `Pagina_Mercado` e `Trocas_Mercado` para não ferir o princípio O (Open/Closed)
#### Pontos negativos:
- Falta um modelo de troca para definir claramente o que é uma troca
---
## Equipe 7
### Tema 1: Jogadores
#### Pontos positivos:
- Arrumaram classes redundantes
- Apresentam gerenciamento de tokens agora
- Mudanças demonstram boa aplicação dos princípios de segregação de interface e responsabilidade única
#### Pontos negativos:
- Falta postura de backend: não devem mudar constantemente; os outros módulos têm que se adaptar
- Falta um verificador de token
- Guardar a senha em texto plano não é bom; deveriam guardar apenas o hash da senha
---
## Equipe 8
### Tema 4: Visualização de cartas
#### Pontos positivos:
- Não mudaram o caso de uso, pois já respeitava os princípios
- Mudaram o diagrama de classes apenas nas relações
- Implementaram um controller adequadamente
- Aplicaram inversão de dependências no controller com `Card Distribution Service` e `Auth Service`
- Pensaram na segregação de responsabilidades
#### Pontos negativos:
- Precisariam na verdade de 2 controllers: um para carta e um para player, mesmo que fosse uma composição
- Não faz sentido ser uma composição por haver apenas 1 `CDS` e `AS`; adiciona mais complexidade sem necessidade
---
## Equipe 9
### Tema 9: Pokédex
#### Pontos positivos:
- Realizaram mudanças em quem chama o quê no caso de uso
- Fizeram alterações nas relações no diagrama de classes
- Modificaram os métodos adequadamente
#### Pontos negativos:
- Não especificaram claramente como estão usando os princípios SOLID, mas souberam responder oralmente como se enquadram (Open/Closed, Inversão de Dependências)
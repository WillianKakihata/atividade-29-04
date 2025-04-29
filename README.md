# Atividade-29-04 - LISTA DE EXERCICIOS - Design Pattern Adapter

### Alunos
#### WILLIAN HIDEAKI KAKIHATA 22015763-2
#### RENAN TONON DE OLIVEIRA 22188153-2

 ### 1  - Explique com suas palavras o que é o padrão adapter e qual problema ele resolve
O padrão Adapter é um padrão de design estrutural que permite que interfaces incompatíveis trabalhem juntas. Ele resolve o problema de integração entre classes ou sistemas que têm interfaces diferentes, mas precisam se comunicar. Em vez de alterar o código existente, o Adapter cria uma "ponte" que adapta a interface de uma classe para a forma esperada por outra.

 ### 2  - Cite um exemplo do mundo real que ilustra o funcionamento do padrão Adapter
Um exemplo do mundo real seria o carregador de um celular. Suponha que você tenha um carregador com uma entrada USB-A, mas seu dispositivo possui uma entrada USB-C. Para conectar o carregador ao dispositivo, você usa um adaptador USB-A para USB-C. O adaptador "adapta" a interface do carregador para a interface necessária pelo dispositivo, permitindo que ambos funcionem juntos.

 ### 3 - Quais são os participantes principais do padrão adapter
Os participantes principais do padrão Adapter são:
- **Target:** Define a interface esperada pelo cliente.
- **Adapter:** Converte a interface de uma classe para a interface esperada pelo cliente.
- **Adaptee:** A classe que possui a interface incompatível e que precisa ser adaptada.

Client: Utiliza a interface do Target para interagir com o sistema.

 ### 4 - Desenhe o diagrama de classe UML do padrão Adapter (na forma de classe)
![Diagrama em branco (2)](https://github.com/user-attachments/assets/3460ccea-d4cc-46a0-9ec4-205fd0a4a2df)


 ### 5 - Liste vantagens e desvantagens do padrão adapter
Vantagens do padrão Adapter:  
- **Reutilização de código:** Permite reutilizar classes existentes sem modificá-las.  
- **Flexibilidade:** Facilita a integração de sistemas que possuem interfaces incompatíveis.  
- **Isolamento:** Reduz o impacto de mudanças, já que adapta a interface sem alterar o código original.  
- **Facilidade de manutenção:** Ao adaptar componentes, a manutenção de sistemas antigos e novos fica mais simples.  
Desvantagens do padrão Adapter:
- **Aumento da complexidade:** Pode introduzir muitas classes adicionais no sistema, tornando o código mais complexo.
- **Desempenho:** A adaptação pode adicionar uma camada extra de processamento, impactando a performance.
- **Excesso de abstração:** Em alguns casos, a adaptação pode ser excessiva, dificultando o entendimento do código.
  
 ### 6  - Qual Princípio do SOLID é mais aplicado no padrão Adapter.  
O princípio Open/Closed (Aberto/Fechado) é o mais aplicado no padrão Adapter.  
Esse princípio afirma que classes devem estar abertas para extensão, mas fechadas para modificação. O Adapter permite adaptar classes existentes (muitas vezes legadas) a novas interfaces sem modificar seu código-fonte, apenas criando uma camada de adaptação (o Adapter).

 ### 7  - Utilizando UML (diagrama de classes), **MODELE** um Adapter que transforma diferentes formatos de dados (XML, CSV. JSON)  em um único formato padrão.  
 ![Diagrama em branco](https://github.com/user-attachments/assets/1d481c97-3aa7-41c6-9bb0-5d1ec0d14c70)

 ### 8  - Como o Adapter contribui para a manutenção de software legado?  
 O Adapter permite que sistemas legados continuem funcionando ao mesmo tempo que se integram com novas tecnologias ou requisitos, sem alterar o código legado.  
Isso é crucial quando o código legado é difícil de modificar (por falta de documentação, risco de quebrar algo, ou até dependências críticas). O Adapter encapsula o legado, oferecendo uma nova interface compatível com o sistema atual.

Exemplo: Um sistema antigo que exporta dados apenas em XML pode ser adaptado para fornecer JSON a um novo front-end, sem mexer no sistema original.
 ### 9  - Dê um exemplo real de biblioteca/framework que usa o padrão Adapter.
Exemplo: JDBC (Java Database Connectivity)  
O JDBC utiliza o padrão Adapter para permitir que diferentes drivers de banco de dados (MySQL, PostgreSQL, Oracle) sigam uma interface padrão (java.sql.Driver).
Cada driver implementa a interface adaptando-se às particularidades do banco. O restante da aplicação usa JDBC de forma genérica, sem saber o banco específico por trás.  

 ### 10 - Quandro **não** usar o padrão Adapter? Justifique com exemplos. 
 Não se deve usar Adapter quando:  
- O código-fonte original pode ser modificado com segurança (ex: você tem controle sobre ambas as classes).
- Há risco de complexidade desnecessária, tornando o design mais difícil de manter.

Exemplo 1: Se você criou tanto a classe cliente quanto a classe alvo, é melhor refatorar diretamente a interface, ao invés de criar uma camada de adaptação desnecessária.  
Exemplo 2: Se múltiplos Adapters começam a ser empilhados (ex: adaptando de CSV para XML, depois para JSON), isso pode indicar um design confuso — talvez usar um padrão como Strategy ou Factory faça mais sentido.  


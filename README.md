# pokeshu_demo
 primeira versão 


Construindo a API:
Utilizando Spring Reactive Web versão 2.7.7, Java SE 17
Padrão de projeto utilizado:
Spring Webflux, Projeto Reactor e Netty.
Forma alternativa de desenvolver APIs
Assíncrona e não bloqueante
Fora do modelo de thread por solicitação
Diminui o número de threads criadas
assíncrona e não bloqueante
Fluxo de dados como um fluxo orientado a eventos/mensagens
Código mantém estilo da programação funcional.

O Mockito é um framework de testes unitários e o seu principal objetivo é instanciar classes e controlar o comportamento dos métodos. O Mockito nos ajuda a criar as classes “dublês de teste”. Dublê de teste é um termo genérico para qualquer cenário em que substituamos um objeto real para o propósito de testes. O dublê fornecido pelo Mockito é o Mock, que é um objeto pré-programado com expectativas de chamadas que ele espera receber e os valores de retorno que se espera que ele devolva. por padrão, remove o junit vintage. 





Atendimento de requisitos do projeto:

a)	Utilização de memória estática para operações em memória.configurado no arquivo Application.properties.

# JPA
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.hibernate.ddl-auto=update

# Tempo máximo em que a resposta deve ser armazenada em cache, em segundos mas podendo adicionar um sufixo para que seja armazenado em dias
spring.resources.cache.cachecontrol.max-age=365d

# Indica que uma vez que se tornou obsoleto, um cache não deve usar a resposta sem revalidá-lo com o servidor.
spring.resources.cache.cachecontrol.must-revalidate=true

# Indica que a mensagem de resposta é destinada a um único usuário e não deve ser armazenada por um cache compartilhado como por exemplo o CDN.
spring.resources.cache.cachecontrol.cache-private=false

# Indica que o recurso é publico e qualquer cache pode armazenar a resposta
spring.resources.cache.cachecontrol.cache-public=true

Está implementado o uso do armazenamento em Cache:
O Spring Framework fornece suporte para adicionar armazenamento em cache de forma transparente a um aplicativo. Em sua essência, a abstração aplica cache aos métodos, reduzindo assim o número de execuções com base nas informações disponíveis no cache. A lógica de cache é aplicada de forma transparente, sem qualquer interferência para o invocador.

b) Chamadas de API utilizando protocolo HTTP:
![image](https://user-images.githubusercontent.com/16144508/209344089-0289c1d7-6e06-480c-af06-832ac9880d4e.png)






c) Testes automatizados.

No diretório do projeto src/test/java, está implementado os três pacotes principais classes padrão Mockit



As anotações no objeto Repository com @Mock. O Mockito instanciará essa classe com valores de retorno padrão para todos os métodos. A classe que será testada deve ser anotada com @InjectMocks. O Mockito instanciará essa classe e injetará todos os @Mock nela.


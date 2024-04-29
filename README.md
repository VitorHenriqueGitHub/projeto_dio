# projeto_dio
projeto azure da dio
Eu inicialmente precisei criar uma conta na azure, inicialmente, eu infelizmente não havia conseguido criar uma conta seguindo o passo a passo da instrututora do curso na DIO, por isso para resolver o problema precisei criar uma conta da azure utilizando meu email institucional, assim me cadastrando na azure for students, uma vez criada essa conta na azure for students, eu consegui acessar os workshops da azure

Após isto precisei ver todas as video-aulas do curso da microsoft para compreender como proseguir no desafio

Agora que eu finalizei todas as video-aulas estou pronto para começar o desafio.
primeiro de tudo precisei acessar o estudio de criação do azure machine learning, onde eu criei um workshop/espaço de trabalho, no qual seu nomei o projeto como "projeto_entrega", uma vez criado eu o acessei. Assim, eu acessei o ML altomatizado criando logo em seguida um novo trabalho de ML altomatizado.

Agora dentro das configurações basicas eu nomei o projeto, assim como seu novo nome de experimento, avançando para a classificação do tipo de tarefa a ser desempenhada pela IA a denominando como do tipo regressão. A seguir eu criei uma base de dados definindo seu nome, sua classificação e seu tipo como sendo Tabular, como demonstrado na aula 4 do modulo eu determinei a criação de uma ativo de dados por url da web, conectando a ia à url https://aka.ms/bike-rentals, partindo então para as configurações deste arquivo da web, onde eu apenas alterei os Cabeçalhos de coluna como sendo "somente o primeiro arquivo tem cabeçalho", avançando para a criação do ativo de dados clicando no botão "criar", uma vez que a base de dados foi criada, eu esperei ela ficar pronta e a selecionei, a seguir cliquei em "avançar" determinando que a coluna de destino seja "rentals(integer)". Uma vez feito isto eu alterei as as definições de configurações adicionais, desmarcando todas as 3 opções, e apenas permitindo os modelos RandomForest e LightGBM.

Agora chegou o momento de definir os limites onde eu defini o Máximo de avaliações, Máximo de avaliações simultâneas, Máximo de nós como sendo igual a 3, o Limite de pontuação da métrica como 0.085, e por fim o Tempo limite do experimento(minutos) e Tempo limite de iteração(minutos) como sendo de 15 minutos, apenas permitindo o encerramento entecipado. 

Feito isto eu defini que o tipo de validação dos dados como sendo de "divisão de validação de treinamento", e deixando a validação percentual de dados como 10, uma vez finalizados as configurações de tarefas, a computação eu tive como preferencia deixar como a padrão, isso é, eu deixei sem servidor, os tipos de maquinas como: CPU e dedicado, e quanto a seu tamanho permiti que fosse: Standard_DS3_v2 (4 núcleo(s), 14GB de RAM, 28 GB de armazenamento, $0.23/hr), tendo um número de instancias de "1" por fim enviando o projeto, o qual eu esperei terminar as execuções para realizar testes.

primeiro verificando suas previsões metricas, evidentemente saindo como o previsto, e verificando seus dados, como por exemplo seus pontos de extremidade os quais tambem não deram problemas.


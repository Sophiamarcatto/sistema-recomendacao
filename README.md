# sistema-recomendacao
# Propósito do ProjetoPropósito do Projeto
##### Este projeto visa desenvolver um sistema de recomendação de filmes que utiliza informações sobre filmes assistidos e não assistidos por um usuário para oferecer sugestões personalizadas. Ao analisar o histórico de visualização, o sistema consegue identificar padrões de gosto e preferências individuais, resultando em recomendações mais precisas e alinhadas aos interesses do usuário.

# Funcionamento do Sistema
##### O sistema foi treinado com dados de 10 usuários, considerando o histórico de filmes assistidos e não assistidos. A partir dessa base de dados, o sistema gera recomendações de filmes que ainda não foram visualizados pelos usuários. Essa abordagem permite que o sistema aprenda a partir das preferências coletivas e individuais, identificando quais características dos filmes são mais valorizadas por cada usuário.

# Algoritmo de Agrupamento Utilizado
##### Para realizar as recomendações, o projeto emprega um algoritmo de agrupamento, que organiza os dados em grupos ou "clusters" com base nas similaridades dos filmes e nas preferências dos usuários. Um exemplo comum de algoritmo de agrupamento é o K-means, que segmenta os dados em k grupos distintos, minimizando a variação dentro de cada grupo.

##### No contexto do sistema de recomendação, o algoritmo analisa características dos filmes, como gênero, diretores, elencos, e avaliações anteriores, além do histórico de visualização de cada usuário. Ao identificar clusters de filmes que compartilham características semelhantes e correlacioná-los com o perfil de cada usuário, o sistema consegue sugerir filmes que têm maior probabilidade de serem do interesse do usuário.

# explicação do código:

##### O código implementa um sistema de recomendação de filmes utilizando o algoritmo de agrupamento KMeans. A primeira etapa consiste em importar as bibliotecas necessárias, que incluem numpy para manipulação de arrays e KMeans da biblioteca scikit-learn para realizar o agrupamento.

##### Em seguida, é definido um conjunto de dados chamado mv_rating, que representa as classificações de filmes por seis usuários. Cada linha do array indica um usuário, enquanto cada coluna representa um filme, onde 1 significa que o filme foi assistido e 0 indica que não foi.

##### O número de clusters (grupos) que o algoritmo KMeans deve identificar é definido como 2. O modelo KMeans é então inicializado com essa configuração e treinado utilizando os dados de classificação.

##### Após o treinamento, o modelo é utilizado para prever a qual grupo cada usuário pertence. O resultado é impresso, mostrando a afiliação de cada usuário a um dos grupos definidos.

##### O código também exibe quais filmes foram assistidos por cada usuário, utilizando a função np.where para identificar os índices dos filmes assistidos.

##### A parte principal do código é a função recomendar_filmes, que recebe um vetor de filmes assistidos pelo usuário, juntamente com os dados de classificação e os grupos. Dentro dessa função, o grupo do usuário é determinado e uma lista de usuários pertencentes ao mesmo grupo é criada. Para cada um desses usuários, os filmes que assistiram são coletados e armazenados em um conjunto para evitar duplicatas.

##### Em seguida, a função remove os filmes que o usuário já assistiu do conjunto de recomendações e ajusta os índices para que comecem de 1, facilitando a leitura. Por fim, a função retorna uma lista ordenada dos filmes recomendados.

##### Um exemplo de uso da função é apresentado, onde um vetor que representa os filmes assistidos por um usuário é passado para a função. Os filmes recomendados são então impressos.


##### Esse sistema proporciona uma maneira eficaz de recomendar filmes com base nas preferências de grupos de usuários, ajudando a melhorar a experiência de visualização ao oferecer sugestões personalizadas.
#### Benefícios do Sistema
#####  O sistema oferece recomendações sob medida, ajudando os usuários a descobrir novos filmes que se encaixam em seus gostos.
#### Eficiência:
##### Ao automatizar o processo de recomendação, os usuários economizam tempo na busca por novos filmes.
#### Experiência do Usuário: 
##### O aumento na relevância das sugestões enriquece a experiência do usuário, incentivando a exploração de novas opções de entretenimento.

## O sistema de recomendação de filmes oferece várias utilidades significativas:

#### Personalização das Sugestões: 
##### Proporciona recomendações que se alinham aos gostos individuais dos usuários, aumentando a satisfação e a probabilidade de visualização.

#### Descoberta de Novos Filmes: 
##### Ajuda os usuários a encontrar filmes que talvez não conhecessem, ampliando suas opções de entretenimento.

#### Otimização do Tempo de Busca: 
##### Reduz o tempo que os usuários gastam procurando filmes, apresentando opções relevantes de forma rápida.

#### Aprimoramento da Experiência do Usuário: 
##### Enriquecer a interação do usuário com a plataforma, tornando-a mais envolvente e agradável.

#### Análise de Dados: 
##### Permite aos desenvolvedores entender melhor as preferências dos usuários e aprimorar continuamente o algoritmo de recomendação.



# Conclusão
##### O sistema de recomendação de filmes desenvolvido neste projeto demonstra uma abordagem eficaz para personalizar a experiência do usuário, utilizando o histórico de visualização e técnicas de agrupamento para oferecer sugestões que refletem os gostos individuais. Ao analisar padrões de comportamento e preferências, o sistema não apenas facilita a descoberta de novos filmes, mas também otimiza o tempo gasto na busca por opções de entretenimento.

##### Além de aprimorar a satisfação do usuário, essa solução fornece insights valiosos sobre tendências e preferências em larga escala, beneficiando tanto os usuários quanto as plataformas de streaming. Com a possibilidade de expansão e melhoria contínua do algoritmo, o sistema tem potencial para se tornar uma ferramenta indispensável na experiência de visualização, promovendo um engajamento maior e incentivando a exploração de conteúdos variados.


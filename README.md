# Recomendar_Filmes
Criando um sistema de recomendação de filmes que analise o histórico de visualização do usuário e sugira filmes com base em preferências semelhantes de outros usuários.

# Sistema de Recomendação de Filmes em Python
Este projeto implementa um sistema simples de recomendação de filmes em Python. O sistema permite aos usuários assistir a filmes e, com base nos gêneros dos filmes que o usuário já assistiu, recomenda outros filmes semelhantes.

## Funcionalidades

Adicionar novos usuários.
Adicionar novos filmes com títulos e gêneros.
Usuários podem assistir a filmes.
Sistema de recomendação que sugere filmes com base nos gêneros dos filmes já assistidos pelo usuário.

## Estrutura do Projeto

movie.py: Contém a definição da classe Movie, que representa um filme com título e gênero.
user.py: Contém a definição da classe User, que representa um usuário que assiste a filmes e mantém uma lista de filmes assistidos.
movie_recommender.py: Contém a definição da classe MovieRecommender, que representa o sistema de recomendação de filmes.
main.py: Arquivo principal do programa, onde exemplos de uso são demonstrados.

## Exemplo de Uso

´´´
# Criando alguns filmes
movie1 = Movie("Inception", "Sci-Fi")
movie2 = Movie("The Matrix", "Sci-Fi")
movie3 = Movie("The Shawshank Redemption", "Drama")
movie4 = Movie("The Godfather", "Crime")

# Criando um usuário e adicionando alguns filmes assistidos
user1 = User("Alice")
user1.watch_movie(movie1)
user1.watch_movie(movie3)

# Criando o sistema de recomendação
recommender = MovieRecommender()

# Adicionando o usuário e os filmes ao sistema de recomendação
recommender.add_user(user1)
recommender.add_movie(movie1)
recommender.add_movie(movie2)
recommender.add_movie(movie3)
recommender.add_movie(movie4)

# Obtendo recomendações para o usuário
recommendations = recommender.recommend_movies(user1)

# Imprimindo as recomendações
print(f"Recomendações para {user1.username}:")
for movie in recommendations:
    print(movie.title)

````

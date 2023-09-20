class Programa:
    def __init__(self, nome, ano, genero):
        self._nome = nome.title()
        self.ano = ano
        self.genero = genero
        self._likes = 0

    def dar_like(self):
        self._likes += 1

    @property
    def likes(self):
        return self._likes

    @property
    def nome(self):
        return self._nome

    @nome.setter
    def nome(self, novo_nome):
        self._nome = novo_nome.title()

    def __str__(self):
        return f'{self._nome} - {self.ano} - {self.genero} : {self._likes} Likes'
class Filme (Programa):
    def __init__(self, nome, ano, duracao, genero):
        super().__init__(nome, ano, genero)
        self.duracao = duracao
    def __str__(self):
        return (f'{self._nome} - {self.ano} - {self.duracao} min - {self.genero} : {self._likes} Likes')

class Serie (Programa):
    def __init__(self, nome, ano, temporadas, genero):
        super().__init__(nome, ano, genero)
        self.temporadas = temporadas

    def __str__(self):
        return (f'{self._nome} - {self.ano} - {self.temporadas} Temporada(s) - {self.genero} : {self._likes} Likes')


class Playlist:
    def __init__(self, nome, programas):
        self.nome = nome
        self._programas = programas

    def __getitem__(self, item):
        return self._programas[item]

    def __len__(self):
        return len(self._programas)

    @property
    def listagem(self):
        return self._programas

    @property
    def tamanho(self):
        return len(self._programas)

lotr = Filme('Senhor dos Anéis: A Sociedade Do Anel', 2001, 178, 'Aventura / Ação')
whale = Filme('The Whale', 2022, 117, 'Drama')
soa = Serie('Sons of Anarchy', 2008, 7, 'Drama / Policial')
sunshine = Serie('Mr.Sunshine', 2018, 1, 'Drama / Histórica')

lotr.dar_like()
whale.dar_like()
whale.dar_like()
whale.dar_like()
soa.dar_like()
sunshine.dar_like()
sunshine.dar_like()

filmes_e_series = [lotr, soa, whale, sunshine]
playlist_fim_de_semana = Playlist('Fim de Semana', filmes_e_series)

print(f'Tamanho do playlist: {len(playlist_fim_de_semana)}')

for programa in playlist_fim_de_semana:
    print(programa)

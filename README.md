# Organizador de Metadados MP3

Aplicativo FastAPI base para organizar e gerenciar metadados de arquivos MP3. Este projeto serve como base para futura implementação de funcionalidades de manipulação de tags ID3.

## Estado Atual

O projeto atualmente consiste em uma aplicação FastAPI minimalista com um único endpoint:

### GET `/`
Retorna uma mensagem de boas-vindas:

```json
{
  "message": "Hello, World!"
}
```

### Tecnologias Utilizadas

- **FastAPI**: Framework web para construção da API
- **Python >= 3.14**: Linguagem de programação

## Planejado para o Futuro

Este projeto tem como objetivo evoluir para um organizador completo de metadados MP3 com as seguintes funcionalidades:

- **Leitura de metadados MP3**: Extrair tags ID3 (título, artista, álbum, ano, gênero, número da faixa) dos arquivos MP3
- **Edição de metadados**: Atualizar tags de metadados para arquivos MP3 individuais ou em lote
- **Organização de arquivos**: Renomear e mover arquivos com base em seus metadados
- **Visualização de coleção**: Exibir informações organizadas sobre sua coleção MP3
- **Busca e filtro**: Pesquisar e filtrar arquivos por atributos de metadados

## Instalação

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/organizador-metadados-mp3.git
cd organizador-metadados-mp3

# Instale as dependências
poetry install

# Ou usando pip
pip install -r requirements.txt
```

## Como usar

```bash
# Iniciar o servidor de desenvolvimento
fastapi dev fast_zero/app.py

# Ou usando poetry
poetry run fastapi dev fast_zero/app.py
```

A API estará disponível em `http://localhost:8000`.

## Roadmap

1. ✅ Estrutura básica do FastAPI - **CONCLUÍDO**
2. 🔲 Implementar leitura de tags ID3 usando biblioteca `mutagen` ou `eyed3`
3. 🔲 Criar endpoints de metadados MP3 (`/mp3/{file_id}`, `/mp3/list`, etc.)
4. 🔲 Implementar edição de metadados
5. 🔲 Adicionar organização/renomeação de arquivos
6. 🔲 Implementar interface de busca e filtro

## Desenvolvimento

```bash
# Executar testes
pytest

# Linting
ruff check

# Formatar código
ruff format
```

## Licença

Este projeto está licenciado sob a licença MIT.
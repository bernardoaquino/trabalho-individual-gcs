# Trabalho GCS Individual - Bernardo Aquino Capello Coelho

## Configuração do Ambiente

### Docker (App/Python, Metabase, MongoDB e PostgreSQL)

Essas foram minhas ações para executar o ambiente de desenvolvimento:

```bash
docker compose up -d
```

## As ferramentas abaixos, incluindo o build do Docker foram todas automatizadas no Github Actions(CI/CD)

### Poetry

Para gerenciar as dependências e pacotes Python usando Poetry, foram realizadas essas etapas

Instalação (Linux):

```bash
python3 -m pip install --user pipx
python3 -m pipx ensurepath --force
pipx install poetry
```

Instalação (Windows):

```bash
python -m pip install --user pipx
python -m pipx ensurepath --force
pipx install poetry
```

Adicionanando Dependências:

```bash
for item in $(cat requirements.txt); do poetry add "${item}"; done
```

#### Publicação do Pacote (Observação):

```bash
poetry config http-basic.pypi <username> <password>
```

> _Devido a restrições de criação de conta na plataforma https://pypi.org/, não é possível publicar o pacote no momento._

### Doxygen (Documentação)

Para gerar documentação usando Doxygen, foram realizadas essas etapas:

Instalação (Linux):

```bash
sudo apt-get install doxygen
doxygen -g
doxygen
```

### Sphinx (Documentação)

Para gerar documentação utilizando Sphinx, foram realizadas essas etapas:

Instalação (Linux):

```bash
sudo apt-get install python3-sphinx
sphinx-quickstart
sphinx-apidoc -o sphinx/ src/
make html
```

Estas instruções foram realizadas essas etapas na configuração do ambiente e na execução das etapas necessárias para o trabalho com Docker, Poetry, Doxygen e Sphinx, conforme mencionado nas suas anotações.

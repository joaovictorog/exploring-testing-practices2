# Explorando Práticas de Teste

Neste exercício, vamos explorar práticas de teste em sistemas reais utilizando a ferramenta [TestMiner](https://andrehora.github.io/testminer).

O TestMiner permite visualizar e analisar testes de software em repositórios do GitHub, fornecendo dados sobre como os projetos organizam seus testes, como eles evoluem entre versões e quais bibliotecas de teste são utilizadas.
Explore a ferramenta antes de começar para se familiarizar com seu funcionamento.

Mais detalhes no GitHub da ferramenta: https://github.com/andrehora/testminer.

---

## Passo 1: Selecionar DOIS repositórios

Escolha dois repositórios reais que possuam testes de software.
Abaixo estão alguns links para ajudá-lo a encontrar projetos interessantes:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

- Tópicos: [ai](https://andrehora.github.io/testminer/#topic:ai), [llm](https://andrehora.github.io/testminer/#topic:llm), [api](https://andrehora.github.io/testminer/#topic:api), [nodejs](https://andrehora.github.io/testminer/#topic:nodejs), [android](https://andrehora.github.io/testminer/#topic:android)

- Por organização: [Google](https://andrehora.github.io/testminer/#google), [Microsoft](https://andrehora.github.io/testminer/#microsoft), [Apple](https://andrehora.github.io/testminer/#apple), [Facebook](https://andrehora.github.io/testminer/#facebook), [Netflix](https://andrehora.github.io/testminer/#netflix), 
[GitHub](https://andrehora.github.io/testminer/#github), [Apache](https://andrehora.github.io/testminer/#apache), [HuggingFace](https://andrehora.github.io/testminer/#huggingface)

## Passo 2: Explorar os repositórios selecionados

Busque os repositórios escolhidos no [TestMiner](https://andrehora.github.io/testminer) e analise os dados de teste gerados pela ferramenta.

## Passo 3: Explicar as prática de teste

Para cada repositório, escolha uma prática ou dado de teste relevante e explique com suas próprias palavras.

---

## Instruções de entrega

1. Faça um `fork` deste repositório (saiba mais sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork. Pode adicionar imagens para enriquecer sua explicação.
3. No Moodle, submeta apenas a URL do seu fork.

---

## Respostas

### Repositório 1 

Repositório: https://github.com/pallets/flask

URL TestMiner: https://andrehora.github.io/testminer/#pallets/flask

Explicação: O Flask mantém os testes bem separados do código-fonte. Na análise do
TestMiner, o projeto possui 36 arquivos de teste e 35 arquivos auxiliares de teste.
Grande parte desses arquivos auxiliares está em diretórios como tests/static,
tests/templates e tests/test_apps, que contêm configurações, páginas, modelos e
pequenas aplicações usadas durante os testes. Essa organização permite simular
situações reais sem misturar os dados e recursos de teste com a implementação da
biblioteca. Além disso, o arquivo .github/workflows/tests.yaml mostra que a suíte
é executada automaticamente na integração contínua.

### Repositório 2

Repositório: https://github.com/psf/requests

URL TestMiner: https://andrehora.github.io/testminer/#psf/requests

Explicação: O Requests possui 10 arquivos de teste e 12 arquivos auxiliares de
teste identificados pelo TestMiner. Um aspecto relevante é a infraestrutura criada
para testar conexões seguras: o diretório tests/certs reúne certificados válidos,
expirados e de autenticação mútua. Assim, o projeto consegue verificar diferentes
cenários de TLS usando recursos controlados e reproduzíveis. O workflow
.github/workflows/run-tests.yml, também reconhecido pela ferramenta, automatiza a
execução desses testes no ambiente de integração contínua.

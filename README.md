# Locust
- O Locust é uma ferramenta opensource para criação de testes via HTTP e outros protocolos.
- Você pode criar testes baseados em códigos python.

### Instalçaão
- Primeiro você necessita instalar o bin do locust que será usado para fazer os testes
    1. Essa é a DOC para a instalação do locust e do seu UI pra ver os gráficos no browser (https://docs.locust.io/en/stable/installation.html)

### Primeiro Teste
- primeiro cria um arquivo com o seguinte modelo.

```python
from locust import HttpUser, task

class HelloWorldUser(HttpUser):
    @task
    def hello_world(self):
        self.client.get("/health/check")
```

- esse exemplo irá usar o endereço passado no UI e irá chamar esse path.
- rodando o comando
```bash
locust -f nomedoarquivo.py
```

DOC: https://docs.locust.io/en/stable/quickstart.html
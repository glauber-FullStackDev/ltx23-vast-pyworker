# ltx23-vast-pyworker

PyWorker da Vast.ai para o endpoint **LTX 2.3 IA2V Personal LoRA** (Vast.ai
serverless). Este repositório é consumido pelo mecanismo `PYWORKER_REPO` do
workergroup Vast: o `start-server` clona este repo, instala `requirements.txt`
e roda `python worker.py`.

O `worker.py` expõe as rotas `/submit`, `/status`, `/health` e `/benchmark`,
fazendo proxy para o model server FastAPI que roda dentro da imagem
`ambienteavatar-ltx23-serverless-vast` em `MODEL_SERVER_PORT` (padrão `18080`).

Este arquivo é o espelho de
`ltx-2.3-serverless-vast/pyworker/worker.py` do repositório
`glauber-fullstackdev/ambienteAvatar`. Mantenha os dois em sincronia ao alterar
o contrato das rotas.
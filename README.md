# Projeto 95 KG — PWA Android

Aplicação de treino 100% estática, sem dependências nem servidor de dados.

## Funcionalidades
- Cinco treinos de musculação com séries, repetições, descansos e cardio.
- Registo de carga/repetições e séries concluídas (rascunho automático).
- Histórico de treinos concluídos.
- Temporizador de descanso com aviso vibratório (quando suportado).
- Registo e gráfico de peso, com meta de 95 kg.
- Armazenamento local, exportação/importação de backup JSON.
- Funcionamento offline após a primeira visita com ligação à internet (service worker).

## Instalar no Android com GitHub Pages
1. Crie um repositório GitHub (pode ser público, já que contém apenas o código e **nenhum dado pessoal**).
2. Envie para a raiz do repositório os ficheiros contidos nesta pasta.
3. Aceda a **Settings > Pages > Build and deployment** e configure **Deploy from a branch**, branch **main**, pasta **/(root)**; guarde.
4. Abra no Chrome Android o endereço HTTPS apresentado em GitHub Pages (normalmente `https://UTILIZADOR.github.io/REPOSITORIO/`).
5. No menu ⋮ do Chrome, escolha **Instalar aplicação** ou **Adicionar ao ecrã principal**.
6. Depois da primeira abertura online, a app pode ser aberta offline.

**Nota:** abrir o ficheiro `index.html` diretamente no telemóvel não ativa a instalação PWA nem o service worker. Precisa de ser servido por HTTPS ou localhost. A publicação no GitHub Pages depende das definições e elegibilidade do repositório.

## Segurança e limites
- Os dados guardam-se só no navegador/dispositivo, não no GitHub.
- Limpar dados do site ou desinstalar poderá eliminar o histórico. Use **Opções > Exportar cópia JSON** periodicamente.
- O histórico de peso começa com 105 kg como valor inicial fornecido pelo utilizador; pode atualizá-lo.
- O plano é uma base de treino, não aconselhamento médico individualizado.
- Não incorpora sincronização entre dispositivos nem notificações em segundo plano.

## Testar localmente num computador
Execute `python -m http.server 8000` nesta pasta e abra `http://localhost:8000` (o suporte a PWA exige origem segura; localhost é considerado seguro).

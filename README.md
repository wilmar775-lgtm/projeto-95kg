# Projeto 95 KG — V2 (prévia funcional)

Esta atualização mantém a aplicação original de treinos e acrescenta perfil, questionário opcional de saúde e biblioteca de 30 exercícios com alternativas.

## Publicar sem mexer na produção

1. Confirma que estás na branch `develop-v2` do repositório `projeto-95kg`.
2. Extrai este ZIP. **Envia todos os ficheiros que aparecem na raiz, não o próprio ZIP.**
3. GitHub → Add file → Upload files → arrasta os ficheiros extraídos → Commit changes na `develop-v2`.
4. Não alteres a branch `main` nem o workflow `deploy.yml`.
5. Para testar sem afetar a app publicada, podes usar um ambiente local (`python -m http.server 8000`) ou criar um site de ensaio separado. GitHub Pages atual está ligado a `main`, não à `develop-v2`.
6. Após testes e quando decidires publicar, cria um Pull Request `develop-v2` → `main`; a publicação atualiza automaticamente.

## O que funciona nesta versão

- 5 treinos da V1, histórico, pesos, temporizador, gráfico e backup V1 preservados.
- Perfil opcional (idade, peso, altura, experiência, disponibilidade, objetivos, avatar, rotina).
- Questionário opcional de saúde com medicamentos e hormonas, alertas prudentes (não diagnóstico).
- 30 exercícios com **esquemas visuais simbólicos**, orientações gerais e pelo menos duas alternativas.
- Novos dados do perfil salvos separadamente na chave `projeto95_profile_v2`; dados V1 continuam em `projeto95_state_v1`.
- Exportação e eliminação do perfil V2.
- Offline através do `sw.js` atualizado.

## Limitações explícitas

Esta é uma **primeira entrega V2 funcional**, não um sistema médico, não um treinador autónomo e não possui ainda imagens anatómicas específicas validadas, fotografias ou vídeos. Os esquemas são simbólicos. Ainda não modifica automaticamente o plano com base no questionário. Não possui integração com smartwatches, localização, ginásios, login ou servidor. A validação de entrada e os avisos não substituem orientação de profissionais.

## Testar

- Abrir `Perfil`, guardar dados, fechar/reabrir o site, confirmar persistência.
- Alterar resposta sobre hormonas e verificar a pergunta complementar.
- Abrir `Exercícios`, consultar alternativas e regressar.
- No separador `Treinos`, consultar guia e regressar ao treino.
- Registar série e peso; garantir que os dados V1 continuam presentes.
- Ativar modo avião após uma primeira abertura online e confirmar abertura offline.
- Testar exportação V1 e V2 separadamente.

**Nota de segurança:** questionários de saúde são dados sensíveis mesmo quando guardados localmente; cópias JSON não são encriptadas. Evita partilhá-las inadvertidamente. Para publicação comercial, é necessário revisão médica/desportiva e de privacidade antes da disponibilização pública.

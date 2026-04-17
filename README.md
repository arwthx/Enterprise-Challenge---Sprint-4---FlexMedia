 🤖 Challenge Flexmedia - Tótem Inteligente (Sprint 4)

Este repositório contém a entrega final da Sprint 4 do Challenge Flexmedia. O projeto consiste em um Tótem Inteligente Interativo projetado para ambientes de visitação (museus, eventos e centros culturais), integrando Inteligência Artificial, Visão Computacional e Análise de Dados para enriquecer a experiência do visitante.

--- RM566697 - Arthur Peixoto Souza

 📝 Contexto do Projeto
O Tótem Inteligente Flexmedia evoluiu de um protótipo técnico para uma solução digital interativa. Ele é capaz de:
1. Interpretar o ambiente via Visão Computacional.
2. Personalizar a jornada do usuário através de um modelo de Machine Learning.
3. Gerar insights de negócio através da coleta e análise de logs de interação (Engajamento, Horários de Pico e Perfis).

---

 🏗️ Arquitetura da Solução
A solução segue um fluxo de dados estruturado em quatro etapas principais:

| Etapa | Descrição | Tecnologia |
| :--- | :--- | :--- |
| Captura | Entrada de dados (idade) e captura de imagem (presença). | OpenCV / Streamlit |
| IA/ML | Classificação e Recomendação baseada no perfil do usuário. | Scikit-Learn |
| Storage | Armazenamento de logs de interação em formato estruturado. | CSV / Pandas |
| Analytics | Geração de gráficos e métricas de engajamento. | Matplotlib |

---

 🧠 Inteligência Artificial
O sistema utiliza um modelo de Árvore de Decisão (Decision Tree) treinado com dados estruturados. 
- Entradas (Features): Idade do visitante e Horário da visita.
- Saída (Label): Recomendação personalizada (Tecnologia, História ou Arte).
- Lógica: A IA identifica padrões comportamentais para sugerir a melhor atração de forma autônoma.

---

 📁 Estrutura de Arquivos
/
├── app.py                 # Interface principal do Tótem (Streamlit)
├── train_model.py         # Script de treinamento da IA e geração de dados
├── gerar_relatorio.py     # Script analítico para geração de gráficos
├── requirements.txt       # Dependências do projeto
├── README.md              # Documentação principal
├── models/                # Pasta onde o modelo (.pkl) é armazenado
├── data/                  # Pasta onde os logs de interação (.csv) são salvos
└── relatorio_graficos/    # Pasta onde as imagens do relatório final são exportadas

---

 🚀 Como Executar o Projeto

 1. Preparação do Ambiente
Certifique-se de ter o Python instalado. Instale as bibliotecas necessárias:
pip install streamlit pandas scikit-learn opencv-python-headless joblib matplotlib

 2. Treinamento da IA
Antes de rodar o Tótem, você deve treinar o modelo para que a pasta models/ seja criada:
python train_model.py

 3. Inicialização do Tótem
Para abrir a interface interativa no seu navegador:
streamlit run app.py

 4. Geração de Relatórios
Após realizar algumas interações no Tótem, execute o script abaixo para extrair os gráficos de métricas:
python gerar_relatorio.py

---

 📊 Relatório Analítico e Métricas
O sistema foi testado simulando um fluxo real de visitantes. Os resultados demonstraram:
- Engajamento: 68% dos usuários utilizaram a câmera para identificação visual.
- Padrões de Uso: Identificação de picos de interação às 10h e 15h.
- Personalização: A IA segmentou com sucesso recomendações para diferentes faixas etárias e períodos do dia.





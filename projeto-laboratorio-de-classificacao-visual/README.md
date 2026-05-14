Readme Modelo Vies Ia Teachable Machine
⚖️ BiasVisionAI: Detecção de Viés em Classificação Visual




📝 Descrição do Projeto

O BiasVisionAI é um modelo experimental de classificação de imagens desenvolvido com o objetivo de demonstrar, de forma prática, como vieses algorítmicos podem surgir em sistemas de Inteligência Artificial quando o conjunto de treinamento apresenta padrões sociais limitados ou enviesados.

O projeto foi construído utilizando o framework Google Teachable Machine e exportado em formato TensorFlow.js, permitindo execução diretamente no navegador sem necessidade de backend. O modelo realiza inferência em tempo real utilizando visão computacional e classificação supervisionada.

A proposta acadêmica do projeto é evidenciar como algoritmos aprendem associações a partir dos dados fornecidos durante o treinamento. Neste caso, o conjunto de imagens foi organizado propositalmente com padrões visuais tendenciosos, permitindo analisar os impactos sociais e técnicos do viés em IA.

O sistema demonstra como classificadores podem reproduzir desigualdades e estereótipos quando treinados com bases de dados não representativas.

🧠 Objetivo Acadêmico

Este projeto foi desenvolvido para a disciplina de Fundamentos de Inteligência Artificial com foco em:

Demonstrar o funcionamento de modelos supervisionados
Evidenciar o impacto do viés em datasets
Discutir ética em IA e justiça algorítmica
Explorar pipelines de treinamento com visão computacional
Aplicar conceitos de Human-in-the-loop
🎭 Classes do Modelo

O modelo foi treinado com duas categorias principais:

Rótulo	Classe	Descrição
Bonito	😀 Bonito	Imagens classificadas com características consideradas positivas no dataset
Feio	😐 Feio	Imagens classificadas com características consideradas negativas no dataset

⚠️ As categorias acima foram utilizadas exclusivamente para fins educacionais e experimentais relacionados à análise de viés algorítmico.

⚠️ Problema de Viés Demonstrado

O experimento demonstra como um algoritmo pode desenvolver padrões discriminatórios quando treinado com dados limitados ou socialmente enviesados.

🔍 Mecanismo do Viés

A seleção restrita de dados reduz a diversidade de exemplos observados durante o treinamento. Como consequência, o modelo aprende padrões incompletos e assume que eles representam toda a realidade.

Quando o dataset prioriza apenas determinados perfis visuais e exclui outros, o algoritmo replica essa assimetria e transforma um recorte parcial do mundo em uma regra geral.

🌍 Consequência Social

O projeto evidencia como sistemas automatizados podem reforçar estereótipos sociais e raciais ao associar determinados perfis visuais a classificações negativas.

Em contextos reais, modelos enviesados podem impactar:

Sistemas de recrutamento automatizado
Ferramentas de reconhecimento facial
Plataformas de crédito e avaliação social
Algoritmos de recomendação
Sistemas de vigilância e segurança

A ausência de diversidade nos dados compromete a imparcialidade das decisões produzidas pela IA.

🛡️ Estratégia de Mitigação

O projeto propõe uma abordagem baseada em Human-in-the-loop, onde especialistas humanos supervisionam continuamente:

Curadoria do dataset
Balanceamento das classes
Revisão ética dos dados
Monitoramento de padrões discriminatórios
Validação das inferências produzidas pelo modelo

Essa estratégia combina capacidade computacional com análise crítica humana para reduzir decisões injustas.

🚀 Tecnologias Utilizadas
Motor de Inferência: TensorFlow.js v1.7.4
Framework de Treinamento: Google Teachable Machine v2.4.14
Linguagem Principal: JavaScript
Formato do Modelo: TensorFlow.js Graph Model
Execução: Client-side (Browser)
Pipeline: Classificação supervisionada por imagens
📁 Estrutura do Projeto
biasvisionai-model/
├── project.tm          # Projeto exportado do Teachable Machine
├── Bonito-!-*.jpg      # Imagens da classe “Bonito”
├── Feio-!-*.jpg        # Imagens da classe “Feio”
└── README.md           # Documentação do projeto
📊 Especificações Técnicas
Parâmetro	Valor
Nome do Projeto	BiasVisionAI
Número de Classes	2
Tipo de Modelo	Classificação de Imagens
Framework Base	TensorFlow.js
Plataforma de Treinamento	Teachable Machine
Execução	Navegador Web
Inferência	Client-side
Objetivo	Demonstração de Viés Algorítmico
🔧 Como Utilizar
Instalação via CDN
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@1.7.4/dist/tf.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@teachablemachine/image@0.8/dist/teachablemachine-image.min.js"></script>
Carregamento do Modelo
const URL = "./biasvisionai-model/";


async function init() {
  const modelURL = URL + "model.json";
  const metadataURL = URL + "metadata.json";


  const model = await tmImage.load(modelURL, metadataURL);


  const predictions = await model.predict(imageElement);


  predictions.forEach(p => {
    console.log(`${p.className}: ${(p.probability * 100).toFixed(2)}%`);
  });
}
💡 Aplicações Educacionais
Demonstração prática de viés algorítmico
Estudos sobre ética em IA
Introdução a Machine Learning supervisionado
Pesquisas sobre fairness e representatividade
Experimentação com TensorFlow.js
Ensino de visão computacional
📚 Conceitos Relacionados

O projeto aborda conceitos importantes da área de IA:

Fairness in AI
Bias Mitigation
Human-in-the-loop
Computer Vision
Supervised Learning
Ethical AI
Dataset Balancing
Responsible AI
⚠️ Considerações Éticas

Este projeto possui finalidade exclusivamente educacional e acadêmica.

As classificações apresentadas não representam avaliações reais sobre indivíduos, aparência ou valor social. O objetivo é demonstrar como modelos de IA podem reproduzir preconceitos existentes nos dados utilizados durante o treinamento.

A utilização de sistemas semelhantes em produção exige:

Auditoria contínua
Validação ética
Conformidade com LGPD/GDPR
Transparência algorítmica
Representatividade nos datasets
📄 Licença

Distribuído sob a licença MIT.

Consulte o arquivo LICENSE para mais informações.

👨‍💻 Autor

Projeto desenvolvido para fins acadêmicos na disciplina de Fundamentos de Inteligência Artificial.

⬆️ Voltar ao início

# quiz-introducao-administracao[quiz_introducao_administracao_30_questoes (1).html](https://github.com/user-attachments/files/32818459/quiz_introducao_administracao_30_questoes.1.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Quiz - Introdução à Administração</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#f3f5f8;color:#172033}
.container{max-width:760px;margin:auto;padding:20px}
header{background:#123b6d;color:white;padding:24px;border-radius:16px;margin-bottom:18px}
h1{margin:0 0 8px;font-size:24px}
.subtitle{opacity:.9}
.progress{height:8px;background:#dce3ec;border-radius:8px;margin:18px 0;overflow:hidden}
.progress-bar{height:100%;background:#1d78d4;width:0;transition:.3s}
.card{background:white;border-radius:16px;padding:22px;box-shadow:0 3px 15px #00000012}
.question-number{font-size:14px;color:#607086;font-weight:bold;margin-bottom:10px}
.question{font-size:20px;line-height:1.4;font-weight:bold;margin-bottom:20px}
.option{display:block;width:100%;text-align:left;padding:15px;margin:10px 0;border:2px solid #dce2ea;background:#fff;border-radius:12px;cursor:pointer;font-size:16px;transition:.2s}
.option:hover{border-color:#1d78d4;background:#f5f9ff}
.option.correct{border-color:#198754;background:#eaf8ef}
.option.wrong{border-color:#dc3545;background:#fff0f0}
.option:disabled{cursor:default}
.feedback{display:none;margin-top:16px;padding:14px;border-radius:10px;line-height:1.4}
.feedback.show{display:block}
.feedback.correct{background:#eaf8ef;color:#146c36}
.feedback.wrong{background:#fff0f0;color:#a61b29}
button.next{display:none;margin-top:18px;width:100%;padding:15px;border:0;border-radius:12px;background:#123b6d;color:#fff;font-size:17px;font-weight:bold;cursor:pointer}
.result{text-align:center}
.score{font-size:42px;font-weight:bold;color:#123b6d;margin:15px}
.restart{padding:14px 22px;border:0;border-radius:10px;background:#123b6d;color:white;font-size:16px;cursor:pointer}
.small{font-size:14px;color:#68758a}
</style>
</head>
<body>
<div class="container">
<header>
<h1>Quiz — Introdução à Administração</h1>
<div class="subtitle">30 questões • Correção imediata</div>
</header>
<div class="progress"><div class="progress-bar" id="bar"></div></div>
<div id="app"></div>
</div>

<script>
const questions = [
["Qual é o significado original atribuído ao termo latino \"minister\"?",["Direção ou tendência para algo.","Subordinação ou obediência.","Liderança e comando absoluto.","Planejamento de recursos financeiros."],1,"O material apresenta minister com o sentido de subordinação ou obediência."],
["Na visão da administração como arte, qual característica é destacada?",["Uso exclusivo do método científico rigoroso.","Busca total pela previsibilidade absoluta.","Exigência de sensibilidade e talento pessoal.","Desenvolvimento de softwares de gestão."],2,"A administração como arte é relacionada à sensibilidade e ao talento pessoal."],
["Quais são as quatro funções fundamentais do processo administrativo?",["Planejar, organizar, liderar e controlar.","Vender, comprar, estocar e distribuir.","Contratar, treinar, demitir e promover.","Pesquisar, fabricar, anunciar e lucrar."],0,"Essas são as quatro funções fundamentais apresentadas no material."],
["Na Escola de Administração Científica de Taylor, qual era a principal ênfase?",["O ambiente externo.","As pessoas e a motivação.","As tarefas do operário.","A tecnologia da informação."],2,"O material apresenta as tarefas do operário como a principal ênfase de Taylor."],
["Qual técnica Taylor utilizava para definir a forma mais racional de executar cada tarefa da produção?",["Dinâmicas de grupo motivacionais.","Pesquisas de clima organizacional.","Estudo de tempos e movimentos.","Flexibilização da jornada de trabalho."],2,"O estudo de tempos e movimentos era usado para racionalizar a execução das tarefas."],
["Qual opção representa uma das fases de ênfase da Teoria Geral da Administração?",["Ênfase na filantropia social.","Ênfase no lazer dos funcionários.","Ênfase na estrutura organizacional.","Ênfase na política partidária."],2,"A estrutura organizacional aparece entre as fases de ênfase da TGA."],
["Qual é um dos propósitos da administração citado no material?",["Reduzir a expectativa de vida humana.","Ignorar o desenvolvimento do país.","Aumentar a satisfação do cliente.","Manter processos obsoletos e lentos."],2,"Aumentar a satisfação do cliente é um dos propósitos citados."],
["Como o material classifica atualmente a antiga visão de \"tomar conta\" de pessoas ou negócios?",["Em plena ascensão no mercado.","Totalmente ultrapassada e obsoleta.","A única forma correta de gerir.","Essencial para a economia digital."],1,"O material classifica essa antiga visão como ultrapassada e obsoleta."],
["Ao planejar o uso de recursos, o administrador busca atingir quais tipos de objetivos?",["Objetivos meramente estéticos.","Objetivos puramente aleatórios.","Objetivos de desempenho.","Objetivos de desestruturação."],2,"O material relaciona a administração à busca de objetivos de desempenho."],
["Qual é a última ênfase apresentada na lista de tendências da evolução histórica da TGA?",["Ênfase na mecanização do campo.","Ênfase no artesanato manual.","Ênfase na burocracia excessiva.","Ênfase em competências e competitividade."],3,"Competências e competitividade aparecem como a última ênfase da lista apresentada."],
["Qual é o objetivo primordial de constituir e manter uma organização?",["Obter lucro financeiro acima de qualquer outra meta.","Garantir emprego vitalício para todos os sócios.","Atingir objetivos específicos de forma coordenada.","Substituir completamente o uso de tecnologia."],2,"O material relaciona a organização à realização coordenada de objetivos específicos."],
["Segundo a definição de Robbins apresentada no material, qual elemento é essencial em uma organização?",["Um único dono com poder absoluto.","Isolamento das metas individuais.","Falta de coordenação consciente.","Coordenação consciente para atingir metas comuns."],3,"A definição destaca coordenação consciente e metas comuns."],
["Segundo Maximiano, qual recurso é responsável por dar vida e ação ao sistema organizacional?",["Recursos humanos, ou pessoas.","Recursos apenas financeiros.","Espaço físico e instalações.","Maquinário sem operadores."],0,"O material destaca as pessoas como o recurso que dá vida e ação ao sistema."],
["O trabalho conjunto permite atingir propósitos que, se tentados de forma isolada, seriam o quê?",["Muito mais fáceis de alcançar individualmente.","Impossíveis de serem realizados individualmente.","Prejudiciais ao desenvolvimento humano.","Dependentes apenas da sorte do mercado."],1,"O material destaca que o trabalho conjunto permite realizar propósitos que seriam impossíveis individualmente."],
["Qual é uma característica principal que define uma empresa?",["Ser obrigatoriamente sem fins lucrativos.","Atuar exclusivamente em caridade.","Ter o lucro como um de seus objetivos fundamentais.","Operar sem planejamento ou estrutura."],2,"O lucro é apresentado como uma característica fundamental das empresas."],
["Como são classificadas as organizações sociais civis conhecidas como ONGs ou OSC?",["Organizações de Primeiro Setor Governamental.","Organizações de Segundo Setor de Mercado Privado.","Organizações de Terceiro Setor da Sociedade Civil.","Empresas de capital aberto na bolsa."],2,"O material classifica essas organizações como integrantes do Terceiro Setor da Sociedade Civil."],
["Como são chamadas as empresas que possuem capital aberto e negociam suas ações em bolsas de valores?",["Sociedades por Quotas Limitadas (Ltda).","Microempreendedor Individual (MEI).","Sociedades Anônimas de Capital Aberto (S.A.).","Associações sem fins lucrativos."],2,"Empresas de capital aberto são apresentadas como Sociedades Anônimas de Capital Aberto."],
["Segundo o material, uma organização é um conjunto de pessoas que atua seguindo qual critério laboral?",["Uma divisão aleatória das tarefas.","Uma divisão criteriosa das tarefas e do trabalho.","Um sistema em que todos executam a mesma função.","Uma estrutura sem responsabilidades."],1,"O material destaca uma divisão criteriosa das tarefas e do trabalho."],
["Qual sigla define as entidades da sociedade civil sem fins lucrativos citadas no material?",["MEI — Microempreendedor Individual.","S.A. — Sociedade Anônima.","OSCIPs — Organizações da Sociedade Civil.","LTDA — Sociedade por Quotas Limitadas."],2,"A sigla apresentada no material para essas entidades é OSCIPs."],
["Para que um conjunto de recursos humanos seja considerado uma equipe de fato, o que é indispensável?",["Apenas presença física no mesmo local.","Competição interna constante.","Ausência de comunicação entre setores.","União de esforços para um propósito comum real."],3,"Uma equipe exige união de esforços em torno de um propósito comum."],
["Qual é um dos desafios para a gestão das organizações modernas citado no material?",["O isolamento total dos mercados internacionais.","A manutenção de estruturas rígidas e lentas.","A administração ética e moral das organizações.","A redução do empowerment dos colaboradores."],2,"A administração ética e moral é apresentada como um desafio da gestão."],
["Segundo Peter Senge, qual alternativa apresenta uma das cinco disciplinas das organizações de aprendizagem?",["Domínio pessoal e visão compartilhada.","Centralização total de todas as decisões.","Fragmentação do pensamento departamental.","Bloqueio da troca de ideias entre equipes."],0,"Domínio pessoal e visão compartilhada estão entre as disciplinas apresentadas."],
["O que deve ser feito para criar uma organização que estimule a aprendizagem e a troca de conhecimento?",["Ignorar as experiências passadas da empresa.","Estimular a ampla troca de ideias e diálogo.","Restringir o acesso à informação estratégica.","Desestimular a experimentação de abordagens."],1,"O material destaca a comunicação fluida, troca de ideias e diálogo."],
["Na sociedade do conhecimento, o que é fundamental para as empresas conseguirem competir?",["Apostar apenas em mão de obra não qualificada.","Ignorar as inovações tecnológicas do setor.","Focar em Capital Humano e Capital Intelectual.","Manter o conhecimento restrito ao topo."],2,"Capital Humano e Capital Intelectual são apresentados como fundamentais."],
["Qual é a principal função do pensamento sistêmico, considerado a quinta disciplina de Peter Senge?",["Analisar os problemas de forma linear e simples.","Integrar as disciplinas e ver o quadro geral.","Separar a aprendizagem em equipe do domínio pessoal.","Fortalecer as barreiras de comunicação interna."],1,"O pensamento sistêmico integra as disciplinas e permite ver o quadro geral."],
["Segundo o material, os planos produzidos pelo planejamento são baseados em quê?",["Decisões tomadas somente após a execução das tarefas.","Objetivos e nos melhores procedimentos para alcançá-los.","Intuições momentâneas sem necessidade de dados.","Critérios aleatórios de mercado e sorte."],1,"Os planos são baseados nos objetivos e nos melhores procedimentos para alcançá-los."],
["No processo de planejamento apresentado, qual é a etapa final dos seis passos citados?",["Verificar a situação atual e os recursos disponíveis.","Analisar as alternativas de ação possíveis.","Escolher a melhor alternativa entre as opções listadas.","Implementar o plano e avaliar todos os resultados."],3,"A etapa final é implementar o plano e avaliar os resultados."],
["No planejamento estratégico, como o material define o conceito de \"meta\"?",["Desejo abstrato de crescimento sem data marcada.","Descrição qualitativa do que a empresa sonha ser.","Mensuração do objetivo em forma de números e prazo.","Ferramenta usada apenas para punir funcionários."],2,"Meta é apresentada como a mensuração do objetivo em números e prazo."],
["Qual é a abrangência do planejamento tático?",["Cada tarefa ou atividade de forma isolada.","A organização como um todo no longo prazo.","Uma determinada unidade, como um departamento.","Exclusivamente o ambiente externo e a economia."],2,"O planejamento tático abrange uma determinada unidade, como um departamento."],
["Qual é um benefício do planejamento citado no material?",["Aumento da improvisação diante de crises.","Foco e direção para os esforços de todos os membros.","Criação de barreiras para inovação e criatividade.","Garantia de que nenhum erro ocorrerá na gestão."],1,"O planejamento proporciona foco e direção aos esforços dos membros da organização."]
];

let current=0, score=0, answered=false;

function render(){
 const q=questions[current];
 document.getElementById("bar").style.width=((current)/questions.length*100)+"%";
 document.getElementById("app").innerHTML=`
 <div class="card">
 <div class="question-number">QUESTÃO ${current+1} DE ${questions.length}</div>
 <div class="question">${q[0]}</div>
 <div id="options">${q[1].map((o,i)=>`<button class="option" onclick="answer(${i})"><b>${String.fromCharCode(65+i)})</b> ${o}</button>`).join("")}</div>
 <div id="feedback" class="feedback"></div>
 <button id="next" class="next" onclick="next()">Próxima questão</button>
 </div>`;
}
function answer(i){
 if(answered)return;
 answered=true;
 const q=questions[current];
 const buttons=document.querySelectorAll(".option");
 buttons.forEach((b,n)=>{b.disabled=true;if(n===q[2])b.classList.add("correct");if(n===i&&i!==q[2])b.classList.add("wrong")});
 const fb=document.getElementById("feedback");
 if(i===q[2]){score++;fb.className="feedback show correct";fb.innerHTML="<strong>Acertou!</strong><br>"+q[3]}
 else{fb.className="feedback show wrong";fb.innerHTML="<strong>Resposta incorreta.</strong><br>Resposta correta: <b>"+String.fromCharCode(65+q[2])+") "+q[1][q[2]]+"</b><br>"+q[3]}
 document.getElementById("next").style.display="block";
}
function next(){
 if(current<questions.length-1){current++;answered=false;render()}
 else{
 document.getElementById("bar").style.width="100%";
 const pct=Math.round(score/questions.length*100);
 document.getElementById("app").innerHTML=`<div class="card result">
 <h2>Quiz concluído!</h2>
 <div class="score">${score}/30</div>
 <p>Você acertou <b>${pct}%</b> das questões.</p>
 <p class="small">Revise as questões que você errou e tente novamente.</p>
 <button class="restart" onclick="current=0;score=0;answered=false;render()">Refazer quiz</button>
 </div>`;
 }
}
render();
</script>
</body>
</html>

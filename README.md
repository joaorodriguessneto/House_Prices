![Imagem inicial](https://github.com/joaorodriguessneto/House_Prices/blob/main/img/imagem_inicial_medium.png)
# 🏡 Projeto de análise de dados imobiliários com previsão do valor de compra (modelo de regressão).      
#### ______________________________________________________________________________________________________________________
## 🔍 Observações relevantes sobre o projeto:

* #### Este projeto foi desenvolvido com a intenção de simular um cenário real dentro de uma empresa de análise de dados. Vale ressaltar que o contexto apresentado é fictício, e a empresa HabitaData Analytics, assim como seu diretor executivo, foram criados apenas para fins ilustrativos. 

* #### Fique à vontade para explorar todo o código e as análises realizadas ao longo do projeto. O Jupyter Notebook contendo o relatório exploratório está disponível neste repositório, logo acima. 


# 🎯 Desafio de Precificação na Compra de Imóveis: 



#### No contexto comercial, quanto mais alinhado ao valor real de mercado for o preço de aquisição, mais competitiva e justa será a precificação na revenda. A transparência no valor praticado fortalece a confiança do cliente e transmite credibilidade à empresa. Essa coerência entre preço e valor percebido é essencial para preservar a imagem da organização, promover relações de confiança com os compradores e assegurar a saúde financeira do negócio a longo prazo. 



#### A HabitaData Analytics me designou a analisar dados imobiliários para apoiar decisões de compra e revenda, com foco em preço e valorização, de acordo com as seguintes características: 

* ##### 1.    Com base nas características estruturais e localizações dos imóveis, qual seria uma faixa de valor considerada adequada para aquisição?

* ##### 2.   Quais atributos físicos ou de localização exercem maior influência na variação dos preços de mercado?

* ##### 3. Existe uma tendência de que imóveis situados em áreas residenciais menos densas apresentem valores médios superiores em comparação com regiões mais densamente povoadas? 

#### ______________________________________________________________________________________________________________________

# 📖 Dicionário de dados fornecido pela empresa: 

 
 * Zona : Classificação geográfica de vendas 
		
      * RL: Zona residencial de baixa densidade
      * RM: Zona residencial de média densidade 

* Area: Área Territorial 

* Qualidade: Qualidade Construtiva

* AnoConstrucao: Ano de Construção do Imóvel

* QualidadeAquecimento: Qualidade do Sistema de Aquecimento

        Ex	Excelente
        Gd	Bom
        TA	Mediano 
        Fa	Aceitável 

 * Banheiros: Quantidade de Banheiros 

* Quartos_t1: Quantidade de Quartos Tipo 1 

* Quartos_t2: Quantidade de Quartos Tipo 2 
      	
* Comodos: Quantidade de Cômodos no Imóvel 
		
* Lareiras: Quantidade de Lareiras no Imóvel 
		
* Garagem: Quantidade de vagas por Veículo 

* Preco: Valor de mercado do imóvel 

# 🛠️ Abordagem Atual da Empresa (Método utilizado atualmente) 


* #### Atualmente, a empresa Beautiful Houses define os preços dos imóveis com base em uma média dos valores praticados no mercado e, em muitas ocasiões, também se apoia na intuição do diretor executivo e da equipe de negócios. 


* #### Como cientista de dados da empresa, nosso objetivo é aprimorar esse processo, tornando-o mais preciso e baseado em evidências. Para isso, será desenvolvido um modelo de machine learning utilizando regressão linear múltipla, capaz de estimar o valor dos imóveis com base em suas características, como área, número de banheiros, entre outras variáveis relevantes. 


# 💡Estratégia de Solução do Problema         



1.   Importar o dataset ;
2.   Verificar o tamanho e a estrutura do conjunto de dados ;
3.   Identificar valores ausentes ou nulos ;
4.   Analisar os tipos de variáveis disponíveis;
5.   Realizar uma análise exploratória dos dados ;


  *   #### Analisar hipóteses 

      *   Imóveis com área construída menor apresentam preços mais baixos ?
      *   Quanto maior o número de banheiros, maior é o preço do imóvel ?
      *   Imóveis mais novos possuem preços mais elevados ?
      *   Imóveis com aquecimento de melhor qualidade tendem a custar mais ?
      *   A quantidade de vagas de garagem influencia no valor do imóvel ?
      *   Presença de lareira está associada a preços mais altos ?
      *   Imóveis situados em regiões de densidade populacional média têm preços mais altos ?
6.    *    O número de cômodos impacta no valor de compra do imóvel ?
      *   O nível de acabamento influencia significativamente o preço final do imóvel ?
 * #### **Obtenção de Insights**

7.  Explorar as correlações entre as variáveis para entender suas relações ;
8.  Preparar os dados para aplicar um modelo de regressão linear múltipla, com o objetivo de prever o valor do imóvel com base em suas características ;
9.  Construir e treinar o modelo de regressão ;
10.  Responder questionamentos do projeto feito pelo diretor executivo:
    *  Qual seria o valor estimado de venda de um imóvel com as seguintes especificações? 

      * Área construída: 8.750 pés²/ft²
      * Nível de acabamento : 6
      * Ano em que foi construído : 1985
      * Quantidade de banheiros : 3
      * Número de cômodos: 7
      * Total de lareiras : 1
      * Vagas disponíveis na garagem : 2
      * Localizado em uma zona residencial de média densidade populacional 

*  Quais atributos do imóvel exercem maior influência no preço final de venda ?

*  Imóveis situados em áreas residenciais com menor densidade tendem a apresentar preços mais elevados do que os localizados em zonas de maior densidade?


11. Conclusão

# 🧠 Principais insights da análise exploratória 


#### Após a análise realizada, foi possível identificar que as características que mais influenciam o preço dos imóveis, dentro do conjunto de dados analisado, são: a localização (zona residencial), o número de banheiros, o número de vagas na garagem e a qualidade do acabamento. 



* ##  Zona Residencial 

![gráfico de barras](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/grafico_preco_zona.png)

#### O gráfico apresenta a distribuição dos preços em função da classificação das zonas residenciais, com os valores no eixo y e as categorias da zona no eixo x.


* ##  Números de Banheiros. 

![gráfico de barras](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/grafico_preco_banheiro.png)

#### Pode-se observar no gráfico que imóveis com dois banheiros são mais caros do que aqueles com apenas um banheiro. A diferença média de preço entre eles é de aproximadamente $36,404, evidenciando a valorização associada ao maior número de banheiros.


![porcentagem números de banheiros](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/porcentagem_numero_banheiro.png)

#### No conjunto de dados analisado, observa-se que o número de imóveis com apenas um banheiro é 26% maior do que o de imóveis com dois banheiros, indicando uma predominância desse tipo. Apesar disso, os imóveis com dois banheiros, embora menos numerosos, apresentam valores médios superiores, refletindo uma valorização associada ao maior número de banheiros.

* ##  Números de Garagens. 

![porcentagem número de garagens](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/porcentagem_garagem.png)

#### Com base na imagem apresentada, observa-se que a maioria dos imóveis possui 2 vagas na garagem (62,3%), seguida pelos que têm 1 vaga (32,9%). Já os imóveis sem garagem representam apenas (3,7%), e aqueles com 3 vagas são ainda mais raros, com apenas (1,1%). Isso indica uma forte predominância de imóveis com 2 vagas, refletindo uma possível valorização desse perfil no mercado analisado.


![grafico de barras](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/grafico_preco_garagem.png)

#### O gráfico mostra que o preço médio dos imóveis aumenta conforme a quantidade de vagas na garagem. Imóveis sem garagem possuem o menor valor médio ($106.772), enquanto os com 3 vagas alcançam o maior valor ($176.029). Isso indica uma clara valorização associada ao número de garagens.


* ##  Qualidade de Acabamento. 

![gráfico de barras](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/grafico_preco_qualidade.png)

#### O gráfico evidencia uma relação positiva entre o nível de qualidade de acabamento e o preço médio dos imóveis. Observa-se que imóveis com qualidade 8 apresentam valores aproximadamente 59% superiores aos de qualidade 4, indicando que a qualidade do acabamento é um fator determinante na valorização do imóvel.


* ##  Ano de Construção do Imóvel. 

![gráfico de barras poluído](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/tabela_ano_construcao_poluido.png)

#### Para melhorar a clareza da análise, foi realizada uma agregação dos dados por década de construção, em vez de utilizar o ano individualmente. Essa abordagem reduziu a poluição visual presente no gráfico original, que apresentava um grande número de barras com valores muito próximos, dificultando a interpretação dos dados. Com a visualização por décadas, tornou-se possível observar tendências mais claras e significativas na variação do preço médio dos imóveis ao longo do tempo, facilitando a compreensão e a comunicação dos insights extraídos.


![grafico de barras ano de construção](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/grafico_ano_construcao.png)

#### No gráfico acima, observa-se que imóveis mais recentes tendem a apresentar valores médios mais elevados, evidenciando que o ano de construção é uma variável relevante na precificação. Por exemplo, os imóveis construídos na década de 2000 possuem  uma diferença de cerca de 40% a mais do que os da década de 1940, reforçando a valorização de construções mais modernas. Destaca-se ainda a escolha pela agregação dos dados por década, em substituição à divisão por ano, o que contribuiu significativamente para a redução da poluição visual do gráfico e facilitou a identificação de tendências ao longo do tempo.

# 📈 Desempenho Financeiro do Projeto 

## MAE e MAPE

*  #### MAE (Erro Médio Absoluto / Mean Absolute Error) ➔ Refere-se à média do desvio entre a estimativa do modelo e o preço real de compra do imóvel. 

*  #### MAPE (Erro percentual médio absoluto / Mean Absolute Percentage Error) ➔ É a média percentual da diferença entre a estimativa do modelo e o valor real do imóvel. 

#### Considerando os conceitos mencionados, a empresa Beautiful Houses atualmente define o preço dos imóveis que pretende comprar com base na média dos valores praticados no mercado, além de levar em conta a percepção do diretor executivo e da equipe de vendas. Com isso, elaborei um modelo inicial (baseline) utilizando a média dos preços do conjunto de dados fornecido pelo diretor executivo, resultando nas seguintes métricas:

## Métrica do modelo atual
![tabela métrica original](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/tabela_metricas_original.png)

*   #### Analisando o MAPE apresentado na tabela acima, observa-se que o método atual de precificação da empresa apresenta um erro médio de 17,57% em relação ao valor real dos imóveis. Nosso objetivo com a criação do modelo de regressão linear é reduzir significativamente esse erro, aprimorando a precisão da precificação e potencializando a rentabilidade da empresa.

## Métrica do modelo de regressão
![tabela métrica modelo de regressão](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/tabela_metrica_apos_teste.png)

#### A análise dos resultados do modelo de regressão linear desenvolvido pela HabitaData Analytics evidencia uma melhoria significativa em relação à metodologia de precificação anteriormente utilizada por essa empresa. Enquanto o processo atual apresentava um Erro Percentual Médio Absoluto (MAPE) de 17,57%, o novo modelo reduziu esse índice para 7,84%, o que representa uma diminuição de aproximadamente 55% no erro médio.  Essa melhoria tem implicações diretas na estratégia de negócio, especialmente no modelo baseado na compra, reforma e revenda de imóveis. Quanto mais precisa for a estimativa do valor de compra, maior a chance de maximizar o lucro na etapa de revenda. Dessa forma, o modelo proposto contribui não apenas para decisões mais assertivas, mas também para o aumento da rentabilidade, ao evitar aquisições com valores acima do ideal.

# 📋 Atendendo às demandas do diretor executivo:

* ### 1º Qual seria o valor estimado de venda de um imóvel com as seguintes especificações? 
      * Área construída: 8.750 pés²/ft²
      * Nível de acabamento : 6
      * Ano em que foi construído : 1985
      * Quantidade de banheiros : 3
      * Número de cômodos: 7
      * Total de lareiras : 1
      * Vagas disponíveis na garagem : 2
      * Localizado em uma zona residencial de média densidade populacional 

    * Com base no modelo de regressão linear desenvolvido em nossa análise, a estimativa pontual para um imóvel com essas características é de aproximadamente US$ 166.069,84.

* ### 2º Quais atributos do imóvel exercem maior influência no preço final de venda?
    * Zona residencial do imóvel
    * Nível de qualidade do acabamento do imóvel
    * Número de vagas da garagem
    * Número de banheiros do imóvel

* ### 3º Imóveis situados em áreas residenciais com menor densidade tendem a apresentar preços mais elevados do que os localizados em zonas de maior densidade?

    * Imóveis em áreas de baixa densidade populacional tendem a ter preços mais altos devido à percepção de maior valor associada à privacidade, exclusividade e qualidade de vida. Esses fatores tornam essas regiões mais atrativas para compradores que buscam conforto, o que contribui para a valorização dos imóveis.

# ✔️ Conclusão

Com base na análise realizada, a HabitaData Analytics desenvolveu um modelo preditivo robusto, capaz de estimar com maior precisão o valor justo de compra de imóveis residenciais. Ao incorporar variáveis como área construída, número de banheiros, ano de construção e localização, foi possível identificar os principais fatores que influenciam os preços no mercado. O novo modelo reduziu o erro absoluto médio (MAE) em 55,18% em relação ao método atualmente adotado, oferecendo estimativas mais confiáveis e alinhadas ao valor real dos imóveis.

Além de alcançar os objetivos propostos, o projeto proporciona à empresa uma ferramenta estratégica para reduzir riscos na compra e tomar decisões mais seguras na revenda, aumentando a rentabilidade. Os resultados reforçam a importância da análise de dados na gestão de ativos imobiliários, promovendo maior competitividade, eficiência operacional e retorno financeiro consistente.





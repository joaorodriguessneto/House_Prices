![Imagem inicial](https://github.com/joaorodriguessneto/House_Prices/blob/main/img/img_inicial.png)
# 🏡 Projeto de análise de dados imobiliários com previsão do valor de compra (modelo de regressão). / Real estate data analysis project with purchase price prediction (regression model).

# 🔍 Observações relevantes sobre o projeto: / Relevant observations about the project:

* ### Este projeto foi desenvolvido com a intenção de simular um cenário real dentro de uma empresa de análise de dados. Vale ressaltar que o contexto apresentado é fictício, e a empresa HabitaData Analytics, assim como seu diretor executivo, foram criados apenas para fins ilustrativos. / This project was developed with the intention of simulating a real-world scenario within a data analysis company. It is important to highlight that the presented context is fictional, and the company HabitaData Analytics, as well as its executive director, were created solely for illustrative purposes.

* ### Fique à vontade para explorar todo o código e as análises realizadas ao longo do projeto. O Jupyter Notebook contendo o relatório exploratório está disponível neste repositório, logo acima. / Feel free to explore all the code and analyses carried out throughout the project. The Jupyter Notebook containing the exploratory report is available in this repository, just above.


# 🎯 Desafio de Precificação na Compra de Imóveis: / Property Purchase Pricing Challenge:


### No contexto comercial, quanto mais alinhado ao valor real de mercado for o preço de aquisição, mais competitiva e justa será a precificação na revenda. A transparência no valor praticado fortalece a confiança do cliente e transmite credibilidade à empresa. Essa coerência entre preço e valor percebido é essencial para preservar a imagem da organização, promover relações de confiança com os compradores e assegurar a saúde financeira do negócio a longo prazo. / In the commercial context, the closer the acquisition price is aligned with the true market value, the more competitive and fair the resale pricing will be. Transparency in the pricing practiced strengthens customer trust and conveys credibility to the company. This consistency between price and perceived value is essential to preserve the organization’s reputation, foster trusting relationships with buyers, and ensure the long-term financial health of the business.

#### ------------------------------------------------------------------------------------------------------------

### A HabitaData Analytics me designou a analisar dados imobiliários para apoiar decisões de compra e revenda, com foco em preço e valorização, de acordo com as seguintes características: / HabitaData Analytics assigned me to analyze real estate data to support purchase and resale decisions, focusing on price and appreciation, based on the following characteristics:

* #### 1.    Com base nas características estruturais e localizações dos imóveis, qual seria uma faixa de valor considerada adequada para aquisição? / Based on the structural characteristics and locations of the properties, what would be an appropriate price range for acquisition?

* #### 2.   Quais atributos físicos ou de localização exercem maior influência na variação dos preços de mercado? / Which physical or locational attributes have the greatest influence on market price variations?

* #### 3. Existe uma tendência de que imóveis situados em áreas residenciais menos densas apresentem valores médios superiores em comparação com regiões mais densamente povoadas? / Is there a trend where properties located in less densely populated residential areas show higher average values compared to properties in more densely populated regions?

#### -----------------------------------------------------------------------------------------------------------

# 📖 Dicionário de dados fornecido pela empresa: / Data Dictionary Provided by the Company: 
* 
    * Zona : Classificação geográfica de vendas / Geographic sales classification
		
        * RL: Zona residencial de baixa densidade / Low-density residential zone
        * RM: Zona residencial de média densidade / Medium-density residential zone

    * Area: Área Territorial /Land area (pés quadrados/ft²).

    * Qualidade: Qualidade Construtiva / Construction quality.

    * AnoConstrucao: Ano de Construção do Imóvel / Year the property was built.

    * QualidadeAquecimento: Qualidade do Sistema de Aquecimento / Heating system quality

        Ex	Excelente / Excellent
        Gd	Bom / Good
        TA	Mediano / Average
        Fa	Aceitável / Fair

    * Banheiros: Quantidade de Banheiros / Number of bathrooms.

    * Quartos_t1: Quantidade de Quartos Tipo 1 / Number of Type 1 bedrooms.

    * Quartos_t2: Quantidade de Quartos Tipo 2 / Number of Type 2 bedrooms.
      	
    * Comodos: Quantidade de Cômodos no Imóvel / Total number of rooms in the property
		
    * Lareiras: Quantidade de Lareiras no Imóvel / Number of fireplaces
		
    * Garagem: Quantidade de vagas por Veículo / Number of parking spaces

    * Preco: Valor de mercado do imóvel / Market value of the property(em dólar/USD)

# 🛠️ Abordagem Atual da Empresa (Método utilizado atualmente) / Current Company Approach (Method Currently Used)

* ### Atualmente, a empresa Beautiful Houses define os preços dos imóveis com base em uma média dos valores praticados no mercado e, em muitas ocasiões, também se apoia na intuição do diretor executivo e da equipe de negócios. / Currently, the company Beautiful Houses sets property prices based on an average of market values and, in many cases, also relies on the intuition of the executive director and the business team.

* ### Como cientista de dados da empresa, nosso objetivo é aprimorar esse processo, tornando-o mais preciso e baseado em evidências. Para isso, será desenvolvido um modelo de machine learning utilizando regressão linear múltipla, capaz de estimar o valor dos imóveis com base em suas características, como área, número de banheiros, entre outras variáveis relevantes. / As the company's data scientist, our goal is to improve this process, making it more accurate and evidence-based. To achieve this, a machine learning model using multiple linear regression will be developed to estimate property values based on their features, such as area, number of bathrooms, and other relevant variables.

# 💡Estratégia de Solução do Problema / Problem-Solving Strategy:


1.   Importar o dataset / Import dataset;
2.   Verificar o tamanho e a estrutura do conjunto de dados / Check the size and structure of the dataset;
3.   Identificar valores ausentes ou nulos / Identify missing or null values;
4.   Analisar os tipos de variáveis disponíveis / Analyze the types of variables available;
5.   Realizar uma análise exploratória dos dados / Perform exploratory data analysis;


  *   #### Analisar hipóteses / Test hypotheses

      *   Imóveis com área construída menor apresentam preços mais baixos / Do properties with smaller built areas have lower prices?
      *   Quanto maior o número de banheiros, maior é o preço do imóvel / Does a higher number of bathrooms increase the property price?
      *   Imóveis mais novos possuem preços mais elevados / Do newer properties tend to have higher prices?
      *   Imóveis com aquecimento de melhor qualidade tendem a custar mais / Do properties with better heating systems tend to cost more?
      *   A quantidade de vagas de garagem influencia no valor do imóvel / Does the number of garage spaces influence the property value?
      *   Presença de lareira está associada a preços mais altos / Is the presence of a fireplace associated with higher prices?
      *   Imóveis situados em regiões de densidade populacional média têm preços mais altos / Do properties located in medium-density population regions have higher prices?
6.    *    O número de cômodos impacta no valor de compra do imóvel / Does the number of rooms impact the property purchase price?
      *   O nível de acabamento influencia significativamente o preço final do imóvel / Does the level of finish significantly influence the final property price?
 * #### **Obtenção de Insights / Insight Generation**

7.  Explorar as correlações entre as variáveis para entender suas relações / Explore correlations between variables to understand their relationships;
8.  Preparar os dados para aplicar um modelo de regressão linear múltipla, com o objetivo de prever o valor do imóvel com base em suas características / Prepare data to apply a multiple linear regression model aiming to predict property value based on its features;
9.  Construir e treinar o modelo de regressão / Build and train the regression model;
10.  Responder questionamentos do projeto feito pelo diretor executivo / Answer the project questions posed by the Executive Director.
    * #### Qual seria o valor estimado de venda de um imóvel com as seguintes especificações? / What would be the estimated sale price of a property with the following specifications?

      * Área construída / Built area: 8.750 pés²/ft²
      * Nível de acabamento / Level of finish: 6
      * Ano em que foi construído / Year built: 1985
      * Quantidade de banheiros / Number of bathrooms: 3
      * Número de cômodos / Number of rooms: 7
      * Total de lareiras / Number of fireplaces: 1
      * Vagas disponíveis na garagem / Garage spaces available: 2
      * Localizado em uma zona residencial de média densidade populacional / Located in a medium-density residential zone

    * #### Quais atributos do imóvel exercem maior influência no preço final de venda / Which property attributes have the greatest influence on the final sale price?
    * #### Imóveis situados em áreas residenciais com menor densidade tendem a apresentar preços mais elevados do que os localizados em zonas de maior densidade / Do properties located in residential areas with lower density tend to have higher prices than those in higher-density zones?


11. Conclusão / Conclusion

# 🧠 Principais insights da análise exploratória / Main insights from the exploratory analysis

### Após a análise realizada, foi possível identificar que as características que mais influenciam o preço dos imóveis, dentro do conjunto de dados analisado, são: a localização (zona residencial), o número de banheiros, o número de vagas na garagem e a qualidade do acabamento. 
### After the analysis was carried out, it was possible to identify that the features that most influence property prices within the analyzed dataset are: location (residential zone), number of bathrooms, number of parking spaces, and quality of finish.

# ----------------------------------------------------------------------------------------------------------

## Zona Residencial / Residential Zone

![gráfico de barras](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/grafico_preco_zona.png)

#### O gráfico apresenta a distribuição dos preços em função da classificação das zonas residenciais, com os valores no eixo y e as categorias da zona no eixo x. Observa-se que imóveis localizados em zonas de baixa densidade possuem preços superiores aos situados em zonas de média densidade. Essa diferença pode ser atribuída ao maior valor percebido em ambientes mais exclusivos e reservados.
#### The graph shows the price distribution based on the classification of residential zones, with values on the y-axis and zone categories on the x-axis. It is observed that properties located in low-density zones have higher prices compared to those in medium-density zones. This difference can be attributed to the higher perceived value of more exclusive and private environments.

## Números de Banheiros. / Number of Bathrooms.

![gráfico de barras](https://github.com/joaorodriguessneto/House_Prices/blob/main/img_README/grafico_preco_banheiro.png)




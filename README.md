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




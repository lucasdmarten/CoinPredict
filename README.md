<h1 align="center">Previsor de criptmoeda (preço e capitalização de mercado)</h1>
<p align="center"> Ferramenta desenvolvida para analisar a estimativa do preço e capitalização de mercado para criptomoedas.</p>


<h1>💻 Sobre o projeto</h3>

<h2>🔨 Tecnologias</h2>  
<p>As seguintes ferramentas foram usadas na construção do projeto:</p>
<ul>
  <li><a href="https://www.coingecko.com/en/api">Pycoingecko</a></li>
  <li><a href="https://facebook.github.io/prophet/">Prophet</a></li>
  <li><a href="https://pandas.pydata.org/">Pandas</a></li>
  <li><a href="https://numpy.org/">Numpy</a></li>
  <li><a href="https://docs.python.org/3/library/datetime.html">Datetime</a></li>
  <li><a href="https://matplotlib.org/">Matplotlib</a></li>
</ul>

<br>
<h2 align=center> Preparando o ambiente virtual.</h2>
<br>

    $ python -m venv venv
    $ source venv/bin/activate
    $ pip install -r requirements

<br>
<h2 align=center> Como rodar este projeto:</h2>
<br>


    identifier: ID da criptomoeda segundo API do geckocoin
    start_timestamp, end_timestamp: Periodo que será utilizado em timestamp
    period: Número de dias de previsão (Prophet)
    
    EXAMPLE:
    >>> identifier = "bitcoin"
    >>> start_timestamp = datetime(2018,5,1)
    >>> start_timestamp = datetime.timestamp(start_timestamp)
    >>> end_timestamp = datetime.timestamp(datetime.utcnow())
    >>> period = 365 #days
    >>> cp = CoinPredict(identifier=identifier,start_timestamp=start_timestamp,
                                end_timestamp=end_timestamp, period=period)
    # Por padrão mcap=True.
    # Se False retorna previsão de preços, se True retorna previsão de capitalização de mercado.
    >>> cp.prophet(mcap=True)
    '''
    
![alt text](https://github.com/lucasdmarten/CoinPredict/blob/master/bitcoin.png)

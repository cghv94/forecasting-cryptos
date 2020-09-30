# forecasting-cryptos

Pronósticos de evolución del precio de 8 criptomonedas seleccionadas (BTC, ETH, XRP, LTC, BCH, BAT, MANA, GNT) mediante un modelo prophet simple para series de tiempo no lineales.

Acerca de la metodología

La información es obtenida mediante scraping de: https://coinmarketcap.com

Se implementa un modelo prophet simple, para series de tiempo no lineales de la forma:

y(t) = g(t) + s(t) + h(t) + e(t)

Donde:

g(t) = tendencia de los modelos (modelo de crecimiento saturado y un modelo lineal por partes) que describe el aumento o la disminución a largo plazo de los datos.

s(t) = modelo para la estacionalidad con la serie Fourier para describir efectos por factores estacionales como la época del año

h(t) = modelo para la estacionalidad para describir efectos por factores estacionales como efectos vacacionales y eventos de gran magnitud (“human-scale” seasonalities)

e(t) = el término de erreor asociado al modelo

El pronóstico se realiza a 365 días a partir de September 23, 2020

Para más información sobre prophet

https://towardsdatascience.com/forecasting-with-prophet-d50bbfe95f91

https://research.fb.com/blog/2017/02/prophet-forecasting-at-scale/

https://github.com/facebook/prophet

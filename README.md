# Actividad 4


Hecha por: Alexy De Jesus Salcedo Tete.

Actividad hecha en bigquerty con datos abiertos, con el objetivo de mostrar el manejo de los conocimientos adquiridos durante el semestre, el data. El data set que se utilizo es áreas deforestadas del choco con este tomamos las categorías necesarias para la siguiente consulta.


## ¿En un municipio especifico cuales son las mayores causantes de la deforestación?

Para esta respuesta se tomo como lugar designado a el municipio de atrato


``` sql
SELECT MUNICIPIO, CAUSA, COUNT(CAUSA) AS CANTIDAD_DE_CAUSA
FROM `Actividad_4.Deforestación` WHERE MUNICIPIO = 'ATRATO'
GROUP  BY CAUSA, MUNICIPIO
ORDER BY CANTIDAD_DE_CAUSA desc 
```
Como vemos se utilizo una consulta en la cual se selecciono el municipio, la causa (a esta misma se le aplico un COUNT para que nos diera el total de los registros de cada causa), se uso el WHERE para especificar cual era el municipio requerido, finalmente se agrupa por causa y municipio y se ordena por el conteo, ( En el caso donde se vea desee cambiar el departamento se cambia en el WHERE entre comillas simples ). 



# DASHBOARD

<iframe width="600" height="450" src="https://lookerstudio.google.com/s/lUHm63m_cOg" frameborder="0" style="border:0" allowfullscreen></iframe>

# Enlaces importantes 

[DATASET](https://www.datos.gov.co/Ambiente-y-Desarrollo-Sostenible/AREAS-DEFORESTADAS-CHOCO/iczg-dyt3) 

# Actividad 4


Hecha por: Alexy De Jesus Salcedo Tete.

Actividad hecha en bigquerty con datos abiertos, con el objetivo de mostrar el manejo de los conocimientos adquiridos durante el semestre, el data. El data set que se utilizo es áreas deforestadas del choco con este tomamos las categorías necesarias para la siguiente consulta.

#
## ¿En un municipio especifico cuales son las mayores causantes de la deforestación?

Para esta respuesta se tomo como lugar designado a el municipio de atrato


``` sql
SELECT MUNICIPIO, CAUSA, COUNT(CAUSA) AS CANTIDAD_DE_CAUSA
FROM `Actividad_4.Deforestación` WHERE MUNICIPIO = 'ATRATO'
GROUP  BY CAUSA, MUNICIPIO
ORDER BY CANTIDAD_DE_CAUSA desc 
```
Como vemos se utilizo una consulta en la cual se selecciono el municipio, la causa (a esta misma se le aplico un COUNT para que nos diera el total de los registros de cada causa), se uso el WHERE para especificar cual era el municipio requerido, finalmente se agrupa por causa y municipio y se ordena por el conteo, ( En el caso donde se vea desee cambiar el departamento se cambia en el WHERE entre comillas simples ). 


#
# DASHBOARD

<iframe
    title="Dashboard"
    width="100%"
    height="auto"
    src="https://lookerstudio.google.com/reporting/1bd347e6-e31b-4af2-ae51-19b583c267d7">
</iframe>

#
# Enlaces importantes 

[DATASET](https://www.datos.gov.co/Ambiente-y-Desarrollo-Sostenible/AREAS-DEFORESTADAS-CHOCO/iczg-dyt3) 

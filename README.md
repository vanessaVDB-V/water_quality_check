# water_quality_check

## Objectif

La qualité de l’eau potable est un enjeu majeur de santé et de protection de l’environnement. L’accès à une eau saine est une priorité pour les autorités publiques.  En France, des contrôles sanitaires sont effectués régulièrement par les Agences Régionales de Santé (ARS) pour analyser les différents réseaux d’eau. Ces contrôles suivent une réglementation stricte, associant des normes européennes et nationales. (Pour en savoir plus, ce référer aux articles L1321-1 à L1321-6 et R1321-10 à R1321-18 du code de la santé publique française et la directive européenne 2020/2184 )

Dans ce rapport, les résultats de ces analyses sont mises à disposition s’appuyant sur la base de données du gouvernement qui compile les prélèvements depuis début 2016.  

## Source de données

Les données proviennent de l'API de hubeau france. 2 API sont disponibles :
- https://hubeau.eaufrance.fr/api/v1/qualite_eau_potable/communes_udi qui recense les communes avec leurs réseaux associés
- https://hubeau.eaufrance.fr/api/v1/qualite_eau_potable/resultats_dis qui recense tous les résultats d'analyses par réseau

L'API autorise un chargement des données par page de 5000 lignes maximum. Ainsi pour une commune, plusieurs pages peuvent être appelées. 
De plus, un chargement de toutes les données dans Power BI n'est pas optimal. En effet l'API compte 96 pages au total, d'où un grand nombre de données. J'ai donc préféré charger uniquement les analyses correspondantes à la commune choisie. Cependant Power BI propose des paramètres dynamiques uniquement pour des sources en Direct Query, ce qui n'est pas possible via une API. Pour le moment, la commune est choisie au niveau du Power Query. 

## Annexe 
L'image présente dans le rapport est libre de droit : Image par Anna de Pixabay.
Les icônes sont aussi libre de droit : Flat by Freepik 

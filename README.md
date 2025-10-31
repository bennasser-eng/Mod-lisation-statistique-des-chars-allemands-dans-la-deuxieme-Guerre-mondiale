# Projet de Statistique : Le Problème des Chars d'Assaut Allemands

## Description
Ce projet applique les méthodes statistiques du célèbre "problème des chars d'Assaut allemands" à l'estimation de la production d'iPhones 3G à partir de leurs numéros de série. Il compare différents estimateurs pour déterminer le paramètre θ d'une loi uniforme discrète.

## Objectifs
- Implémenter et comparer différents estimateurs de θ
- Étudier les propriétés (biais, variance, EQM) de ces estimateurs
- Appliquer la méthode à des données réelles (numéros de série d'iPhones)
- Valider l'hypothèse d'uniformité des numéros de série

## Méthodes Statistiques Implémentées

### Estimateurs Comparés
1. **Estimateur des moments** : `θ̃ₙ = 2X̄ₙ - 1`
2. **Estimateur basé sur la médiane** : `θ̃'ₙ = 2Médiane - 1`
3. **EMV (Maximum de Vraisemblance)** : `θ̂ₙ = X*ₙ` (maximum observé)
4. **Estimateur graphique** : par régression linéaire sur le graphe de probabilités
5. **Estimateur corrigé** : `θˇₙ = (X*ₙⁿ⁺¹ - (X*ₙ-1)ⁿ⁺¹)/(X*ₙⁿ - (X*ₙ-1)ⁿ)`

### Propriétés Étudiées
- Biais et erreur quadratique moyenne (EQM)
- Intervalles de confiance asymptotiques
- Performance pour différentes tailles d'échantillon


## Résultats Clés

### Performance des Estimateurs (θ = 1000, n = 100)
| Estimateur | Biais | EQM |
|------------|-------|-----|
| Moments | 0.24 | 3455.58 |
| Médiane | 2.71 | 10119.33 |
| EMV | -9.21 | 185.65 |
| Graphique | -6.78 | 2097.07 |
| Corrigé | 0.20 | **102.87** |

### Application aux iPhones
- **Production totale estimée** : 14,887,670 iPhones
- **Test d'uniformité** : p-value = 0.9155 → hypothèse d'uniformité non rejetée

# Conclusions Principales
## Résultats Théoriques

    L'estimateur corrigé offre le meilleur compromis biais-EQM

    L'EMV est simple mais biaisé (sous-estimation systématique)

    Les intervalles de confiance sont fiables pour n suffisamment grand

## Application Pratique

    Méthode validée sur les données réelles d'iPhones

    Estimation robuste de la production totale

    Hypothèse d'uniformité des numéros de série confirmée

# Auteurs

Bennasser Ahmed , Hasbouni, Mouret
*Projet de Statistique - 4 avril 2025*

# Perspectives
    Application à d'autres problèmes d'estimation industrielle

    Développement d'intervalles de confiance exacts

    Étude de robustesse face aux violations d'hypothèses
    

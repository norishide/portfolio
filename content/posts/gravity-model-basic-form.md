---
title: "[5] The Basic Form of the Gravity Model"
date: 2026-07-22
draft: false
math: true
tags: ["science of science", "gravity model"]
summary: "Researchers flow between topics the way trade flows between cities: in proportion to mass, discounted by distance. A minimal gravity model — and what its residuals reveal."
---

In studies of trade, migration, and commuting, the gravity model is the classic first approximation: the flow between two places grows with their masses and shrinks with the distance separating them. The same form can describe researchers moving between topics.

$$T_{jk} = G \cdot \frac{M_j \, M_k}{d_{jk}^{\gamma}}$$

| Symbol | Definition |
|---|---|
| \(T_{jk}\) | Flow of researchers moving from topic \(j\) to topic \(k\) (people per period) |
| \(M_j\) | Mass of the origin: the number of researchers active in topic \(j\) |
| \(M_k\) | Mass of the destination: the momentum of topic \(k\) |
| \(d_{jk}\) | Distance between topics \(j\) and \(k\) in knowledge space |
| \(\gamma\) | Strength of distance decay (estimated from data) |
| \(G\) | Scale constant |

## Expressing each term

**Origin mass \(M_j\).** The number of researchers publishing in topic \(j\) at time \(t\): \(N_j(t)\). Used as is.

**Destination mass \(M_k\).** Citation counts are only knowable after the fact, so use a momentum that is observable at time \(t\) instead:

$$M_k(t) = \frac{\Delta P_k(t)}{P_k(t)}$$

where \(P_k(t)\) is the cumulative number of papers in topic \(k\) and \(\Delta P_k(t)\) is the number of new papers in the most recent period — that is, the growth rate. The inflow rate of new entrants would work as an alternative.

**Distance \(d_{jk}\).** Represent each topic as a vector and define

$$d_{jk} = 1 - \cos(\mathbf{v}_j, \mathbf{v}_k)$$

where \(\mathbf{v}_j\) is the word-distribution vector from LDA, or the centroid of the topic's paper embeddings. In its simplest version the distance can even be one-dimensional: the score gap \(|s_j - s_k|\) along a basic–applied axis.

**Decay \(\gamma\).** The estimation target. Fit both the power form \(d^{-\gamma}\) and the exponential form \(e^{-\gamma d}\), and keep whichever fits the data better. The magnitude of \(\gamma\) is itself an estimate of the strength of the pivot penalty.

## How to use it

Aggregate the observed flows \(T_{jk}\) from the data — who moved from which topic to which, and when — and place them on the left-hand side. Taking logs turns the model into a linear regression:

$$\ln T_{jk} = \ln G + \alpha \ln M_j + \beta \ln M_k - \gamma \ln d_{jk} + \varepsilon_{jk}$$

The heart of the model is the pair \(\beta\) (sensitivity to momentum) and \(\gamma\) (the friction of distance). And the routes whose residuals \(\varepsilon_{jk}\) are large and positive — the paths along which more people flowed than the model predicts — are the trails of "the people who set out walking toward Seta."

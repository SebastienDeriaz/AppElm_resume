# TSM_AppElm

deux parties 

7/14 électrotechnique -> machine électrique

7/14 hautes fréquences -> ondes

théorie puis application sur un logiciel fem

## Examen 

- En deux parties avec deux pages de résumé ( plutôt manuscrit ou note informatique et personnel) une feuille recto-verso.

1. Basse fréq
   1. une simulation d'un dispositif et décrire quel type de simulation (les grandeur en jeu ) 
   2. dimensionner un isolant avec une simulation (quel type de simulation)
   3. exemple des différentes simulations 
   4. rot div ,...
2. Haute fréq
   1. paramètre d'une antenne
   2. mesure d'une antenne à commenter (cas d'antenne)
   3. Calculer distance max de communication entre émetteur et récepteur antenne (Friss)

## Evaluation

2 Rapports de labo (50%) 

examens (50%)

 ## info

Le champs D est la conséquence de E (tension)

Le champs B est la conséquence de H (courant)

Les iso valeurs sont des lignes avec la même valeurs en tout point

Sources en électrostatique : charges ou potentiels 

Sources en magnétostatique : courant ou aimant

La différence entre le gain réalisé et le gain IEEE, le gain IEEE ne prend pas en compte d'éventuelles désadaptation de l'antenne (Hypothèse théorique d'une antenne parfaitement accordée). Le gain réalisé lui prend en compte cela (mesure réelle)

## Résumé

### Math

- maxwell
- rot
- div
- grad

### simulation

- électrostatique (tension et ou potentiel fixe)
  - $\Delta V = \frac{\partial^2V}{\partial x^2}+\frac{\partial^2V}{\partial y^2} = 0$ (équation de Laplace)
  - dimensionnement d'un isolant
  - mesure sans contact (capteur capacitif)
- électrocinétique (tension variable en fonction du temps)
  - $\sigma \cdot \Delta V = 0$ (le $\Delta V$ et l'équation de Laplace)
  - connecteur (pin male et femelle)
- magnétostatique (courant fixe)
  - $(\frac{\partial A_z}{\partial x^2}+\frac{\partial A_z}{\partial x^2}+\frac{\partial A_z}{\partial z^2})\vec{k} = -\mu J_z \vec{k}$  (équation de poisson)
  - haut-parleur (avec courant fixe dans la bobine)
  - capteur magnétique
- magnéto transitoire (courant variable)
  - moteur et générateur électrique
- magnéto harmonique (courant sinusoïdal)
  - capteur par courant de foucault

### Equation utile pour la simu

1. Electro...
   1. $\vec{rot}\vec{E}=\vec{0}$
   2. $Div \vec{D} = \rho$ @ $\rho$ densité de charge (nulle si statique) 
   3. $\vec{D}=\epsilon \cdot \vec{E}$ @ $\epsilon$ est une constante
   4. en découle $\vec{E}=-\vec{grad}\space V$ 
2. Magnéto...
   1. $\vec{rot}\vec{E} = - \frac{\partial \vec{B}}{\partial{t}}$
   2. $\vec{rot}\vec{H} = \vec{J}$
   3. $\vec{H}=\frac{1}{\mu}\vec{B}-\vec{H_c}$ @ $\mu$ perméabilité, $H_c$ champ coercitif de l'aimant
   4. $Div\vec{B} = 0$ 
   5. en découle $\vec{B} = \vec{rot}\vec{A}$ 

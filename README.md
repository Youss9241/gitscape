Résultats d’erreurs ESLint

Pour test ESLint, j’ai d’abord mis des erreurs dans mon fichier app.js volontairement. Par exemple, j’ai oublié des points-virgule

Quand j’ai lancé la commande : npx eslint app.js

le resultat cetait app.js
  1:7  error  Missing semicolon                      semi
  4:1  error  Expected indentation of 2 spaces       indent
  5:1  warning  Unexpected console statement         no-console
  6:1  error  Expected indentation of 2 spaces       indent
  7:1  warning  Unexpected console statement         no-console
  8:1  error  Missing semicolon                      semi
✖ 6 problems (4 errors, 2 warnings)

2 - warning utilisation de consol.log qui est correcte mais signalé
1- les erreurs venaient des points virugles surtout et indentation incorrecte

ensuite pour :npx eslint --fix app.js

Pour corriger automatiquement les erreurs que ESLint pouvait fixer.
Après ça, le fichier app.js ne contient plus d’erreurs critiques et respecte bien les règles du projet. J’ai aussi configuré Husky pour que tout code non conforme bloque le commit

---
layout: page
title: TroubleShooting
---

<div class="texteLong" lang="fr">
            
              <div> <div> <div> <div> <p>
                        <strong>- J'ai une erreur 503:</strong>
                      </p> <p>L'erreur 503 est renvoyée par le serveur Jetty lorsqu'il y a un conflit avec la machine Java. Cela signifie qu'il faut télécharger une version d'Isilex "sans Java".</p> <p>
                        <strong>- J'ai uploadé un corpus XML et j'ai un problème avec IsiCorpus:</strong>
                      </p> <p>IsiCorpus est destiné à l'usage de ceux qui ne veulent pas travailler XML mais l'exploiter quand même: vous ne pouvez télécharger que des fichiers au format .txt. Si vous possédez des corpus XML, il faut en faire des bases (dans le répertoire data) et les exploiter dans vos propres routines XQuery. En voilà une très simple qui affiche votre corpus sur une page ISILEX:</p> <pre>1. declare %rest:path('/monAppli') <br clear="none">2. %output:method('xhtml') <br clear="none">3. function isilex:monAppli()<br clear="none">4. { <br clear="none">5. isi:template<br clear="none">6. ( for $x in db:open('[MASUPERBASE]')/[ROOT] return $x ) <br clear="none">7. }; </pre> </div> </div> </div> </div>
            
          </div>
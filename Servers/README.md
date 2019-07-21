## LE DEPOT SERVER EST INDISPENSABLE POUR LES PROJETS AVEC SERVLET ET TOMCAT

Attention
dans le fichier server/server.xml il doit y avoir une seule fois la balise < Context docBase="TpSuiviDesRepas" path="/TpSuiviDesRepas" reloadable="true" source="org.eclipse.jst.jee.server:TpSuiviDesRepas"/>
Sinon vous aurez un bug du style:
Tomcat server error
‘Publishing to Tomcat v7.0 Server at localhost…’ has encountered a problem.
Could not publish server configuration for Tomcat v7.0 Server at localhost. Multiple Contexts have a path of “/MyProject”.

Correction: aller dans le fichier server/server.xml
– Regardez les balises: il doit y avoir plusieurs fois la balise <Context docBase="TpSuiviDesRepas" path="/TpSuiviDesRepas" reloadable="true" source="org.eclipse.jst.jee.server:TpSuiviDesRepas"/>
Il faut n'en garder qu'une seule. Enregistrer, lancer le servlet.

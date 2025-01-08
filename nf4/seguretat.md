# Seguretat a Wordpress

![image](https://github.com/XaSaFa/MP08-23-24/assets/110727546/634310a7-af05-44e5-9005-17336d542d52)

Tot i que la gran comunitat de Wordpress fa que sigui un dels CMS més segurs, al ser el CMS més utilitzat això fa que sigui l'objectiu continu d'atacs.

![image](https://github.com/XaSaFa/MP08-23-24/assets/110727546/fefab037-612f-405b-b86e-08d6a15790c6)
Dades de la web sucuri.net 

Anem a fer un repàs dels consells per assegurar la nostra web:

## Mantenir la web actualitzada

![image](https://github.com/XaSaFa/MP08-23-24/assets/110727546/8c2ab837-dda2-44fd-8315-2d7170ba39b0)

Molta gent pensa que quan s'ha penjat la web ja està tota la feina feta... En el cas de Wordpress això no és així.

L'aspecte primordial a l'hora de mantenir una web creada en Wordpress segura és actualitzar-la.

![image](https://github.com/XaSaFa/MP08-23-24/assets/110727546/3185694a-c5b6-4641-a18c-d0b70fcb7fc2)

Quan diem actualitzar ens referim a mantenir actualitzats els següents aspectes:

- El programari de Wordpress.
- Els temes.
- Els plugins.

Qualsevol element sense actualitzar és susceptible de ser atacat per agents malintencionats.

## Usuaris de Wordpress

Comprova que els usuaris de Wordpress tenen el perfil que hauríen de tenir, sobretot comprova que els usuaris administradors són els que han de ser.

## Contrasenyes segures

Com amb qualsevol altre aplicació protegida per contrasenya ens hem d'assegurar que les contrasenyes utilitzades pels usuaris són prou segures i apoder ser no són repetides a altres serveis.

## Administrador de Wordpress

L'administrador, a més de tenir una contrasenya segura, és interessant que no tingui com a nom d'usuari el que ve per defecte a Wordpress, que és "admin".

Això és per evitar atacs de scripts de força bruta contra la pàgina web.

## Utilitza només temes i plugins de confiança

La comunitat de Wordpress té una "store" per a temes i plugins, el repositori de Wordpress.

Al repositori té accés tota la comunitat i si en algún moment hi ha algun software sospitós es treurà del repositori.

A més al repositori podeu veure si fa temps que no s'actualitza el software, això ens indica si un desenvolupament està mort o obsolet, en aquest cas no l'instal·larem.

## Eliminar temes i plugins que no s'utilitzen

Quan instal·lem plugins o temes estem afegint codi al directori de Wordpress, moltes vegades no utilitzem els temes o plugins però no els eliminem de la nostra web.

És preferible esborrar tot el que no necessitem pel correcte funcionament del nostre lloc web.

## Actualitzar el programari del servidor

![image](https://github.com/XaSaFa/MP08-23-24/assets/110727546/121f44f5-00d7-4f2e-bd80-6f7e44d34842)

Wordpress funciona gràcies a PHP, per aquest motiu és important mantenir la versió de PHP del nostre servidor actualitzada a la versió recomanada per Wordpress.

També és important actualitzar la Base de dades que utilitzem a les versions recomanades.

![image](https://github.com/XaSaFa/MP08-23-24/assets/110727546/abeb4da4-dff9-4348-a7c7-7340b08b5b20)

## Fes còpies de seguretat

![image](https://github.com/XaSaFa/MP08-23-24/assets/110727546/06721ac6-d40e-4eba-891b-2ac134f7a5f2)

La informació de la web està dispersa entre la base de dades i el directori de Wordpress.

Utilitza un plugin de còpies de seguretat per guardar una còpia en serveis online com Dropbox o Google Drive i, a més, fes alguna còpia local de tant en tant.

Aquí teniu el típic [article](https://blogvault.net/5-best-wordpress-backup-plugins/) dels 10 millors plugins de Wordpress a 2023.

## Utilitza HTTPS, no HTTP

![image](https://github.com/XaSaFa/MP08-23-24/assets/110727546/dda76044-43a5-4e17-80e1-91fb8531a163)

A dia d'avui les webs han d'utilitzar el protocol HTTPS (HyperText Transfer Protocol Secure), això fa que la comunicació entre el client i el servidor estigui encriptada.

El protocol HTTPS parteix de la base de que la pàgina web a la que volem accedir pertany al domini que hauria de ser, per això utilitza claus de verificació.

Si voleu conèixer més sobre el protocol podeu llegir aquest [article](https://www.cloudflare.com/es-es/learning/ssl/why-is-http-not-secure/).

## Utilitzar claus d'encriptació de Wordpress

El fitxer wp-config.php conté unes claus d'encriptació per a les cookies d'usuaris.

Exemple:

![image](https://github.com/XaSaFa/MP08-23-24/assets/110727546/5ab9ed11-8dd6-4762-a03f-374c3641e032)

Si supossem que estim patint un atac canviant aquestes claus podem fer que els usuaris de Wordpress hagin de tornar a fer login a la web per accedir, enlloc de guardar-se la sessió.

## Utilitzar l'autenticació de dos factors

Una bona forma d'evitar que un hacker pugui esbrinar la nostra contrasenya i accedir a Wordpress és obligar a utilitzar seguretat de dos factors, això s'aconsegueix utilitzant un plugin.

## Utilitza un plugin de seguretat de Wordpress

Hi ha opcions de seguretat que ens obliguen a modificar els fitxers PHP de Wordpress, alguns plugins de seguretat fan aquesta feina per nosaltres, podem escollir un dels molts plugins que hi ha.

## Verifica el teu server

Hi ha serveis online que analitzan la teva web i busquen problemes de seguretat, per exemple [sucuri.net](https://sitecheck.sucuri.net/).

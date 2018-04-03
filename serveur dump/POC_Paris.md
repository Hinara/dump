
Paris a du faire la rentree PSO
Il y avait 50 etudiants, 30 avec le lenovo epitech, 15 avec un pc perso.

Materiel:
- un tinkerboard (un raspberry-like avec du Gbit). Dessus, un netboot, avec une iso de fedora, et une unbuntu (au cas ou la fedo marchait pas).
- des clefs USB bootable avec l'iso fedora (au cas ou le netboot ne marchait pas).

Il faut prevoir les 2 solutions, car pour certains pc, une des 2 methode n'a pas marchee.

Pour les etudiants avec un pc perso, il a fallu l'intervention de plusieurs minutes d'un assistant pour chacun.
Le plus gros probleme est le SecureBoot a desactiver (a priori active par defaut sur les pc windows).
La methode est differente d'un pc a l'autre (ca va, d'aller dans le BIOS et desactiver, a, faire un truc dans windows pour activer le bios, set un pass admin, puis desactiver le secureboot).
 
Il y en a 2, ou il n'a pas ete possible d'installer, ni la fedo, ni ubuntu (ils ont fini avec une Vm sur leur Windows). Un sous mac, qui a aussi une VM (on a annonce qu'on gerais pas les MAC).
 
Certains PC n'ont jamais voulu booter sur le reseau, d'autres n'ont jamais pu sur clef USB, il est donc indispensable d'avoir au moins 2 solutions pour dumper). 
Ils ont deja releve quelques eceuils a eviter (du genre faire l'install en anglais, pas en francais, ou ne pas installer gnome-wm ca pete l'install, pas mettre de partitions lvm).
 
Ensuite, une fois que tous les PC avaient un linux.
Ils ont fait dl et lancer les scripts, fait par alexandre je crois, present sur le github content. Scripts qui installent tous les packages et les scripts qu'il faut pour avoir un pseudo dump qui marche.
 
En gros, ca dl 5Go (a ce qu'on m'en a dit). Sur le wifi a 50-100 personnes c'est pas possible. Il faudra mettre les packages sur l'iso.
 
Il faut aussi prevoir de rajouter l'install de windows au moment du dump, si elle se fait apres, l'install de windows pete le grub.
 
Pour les etudiants qui ont pas de wifi a 5Ghz, il faut qu'on donne un modele de dongle wifi compatible.
 
Il faut qu'on consulte tous les chefs de matiere pour leur demander les packages dont ils ont besoins (par ex, en ce moment, il manque les kernel headers pour vmware).
 
Mon idee, surtout sur les grosses villes, c'est de dumper 30-50 clefs USB. Baser l'install principalement la dessus, et mettre le tinkerboard en renfort
 
Materiellement, pour deployer tout ca, il va falloir, par ville:
Un tinkerboard avec une sdcard qui boost bien
Un duplicateur USB pour dumper la chiee de clef usb a dumper.
Logiciellement:
Mettre a jour l'iso pour qu'elle contienne tous les packages qu'on veut installer, et qu'ils soient au minimum a jour.
Reussir a integrer l'install de windows. Ca va etre le plus dur, mais c'est pas indispensable pour la rentree prochaine.
 
Avoir un systeme pour pouvoir update les tinkerboard a distance (l'assistant m'a propose du puppet).
Faire en sorte que les villes puissent set le wifi, et avoir le statut de leur tinkerboard. Si jamais la machine perd le wifi et que localement ils peuvent pas debug, on aura l'air con.
 
Vis a vis des tech0. Je sais pas a quoi ressemblent les documents qu'on leur presente, mais faut etre bien precis sur le fait qu'on assume pas du tout la situation degradee d'un etudiant qui a un pc de merde, avec un linux qui marche pas bien, ou qui est au fond d'une VM.
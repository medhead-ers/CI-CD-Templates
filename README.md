<div align="center">
<img  width="75" src="project-icon.png" />
<br>
<br>
<h1>Medhead ERS CI/CD Templates</h1>
</div>

<br>
<br>

Ce dépot contient les templates CI/CD associés à l'organisation MedHead ERS. Ils ont pour objectifs d'être réutilisés
dans les différents repositories de l'organisation.

## Description

| Pipeline          | Description                                                                                                                                                                         |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Build and Test    | Build l'application à l'aide de maven et déclenche les tests automatisés (mvn package). Si les tests ne sont pas tous valide, la pipeline déclenchera une erreur (+ mail d'alerte). |
| Static Analysis   | Déclenche les tests automatisés avec le profil *coverage*. Les résultats seront transmis à la plateforme SonarCloud pour analyse.                                                   |
| Package on Github | Créé un artefact `.jar` avec le tag de version indiqué pour la release.                                                                                                             |
| Publish to Docker | Créé et publie sur le compte docker medhead ERS l'image docker associé à la release (embarque le `.jar` prêt à l'emploi).                                                           |

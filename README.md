# TP5-Routage-avec-React-Tristan-Chloe


## Ré-implémenter le composant Ré-implémenter le composant ```Link```

### 1. Comment fait-on une redirection avec ```react-router``` ?

On a accès à cet objet en mettant à jour ```history``` avec la page de redirection. Pour cela on va utiliser la fonction ```useHistory``` qu’on va devoir importer dans le code et qui va nous permettre de récupérer l’historique.


### 2. Après avoir lu la documentation correspondante, décrivez le fonctionnement de cette fonction.

C’est un crochet nous permettant d’accéder à l’instance de l’historique nécéssaire pour notre redirection.


### 3. En utilisant cette fonction, devez-vous implémenter le ```CustomLink``` composant sous la forme d'une fonction ou d'une classe ?

On doit donc implémenter le composant CustomLink sous la forme d’une fonction.


### 4. Faites l'implémentation de ```CustomLink```, ajoutez les ```propTypes```, testez la dans une codesandbox et copiez votre implémentation de ```CustomLink``` dans ce document.
```
function HomeButton() {
  let history = useHistory();

  function CustomLink() {
    history.push("/home");
  }

  return (
    <button type="button" onClick={CustomLink}>
      Go home
    </button>
  );
}
```


## Ré-implémenter le composant Route

### 5. Reprenez les questions 2 à 4 avec ```withRouter```
Le withRouter permet d’avoir accès aux propriétés d’history. Il va passer les props ```location``` , la ```match``` et l’```history``` au composant encapsulé.
On doit l’implémenter sous la forme d’une classe.

### 6. Dans la documentation de la react-router, trouvez trois hooks permettant d'obtenir les variables ```history```, ```location``` et ```match```.
Les trois hooks permettant d’obtenir les variables ```history```, ```match```, et ```location``` sont : ```useHistory``` pour l’```history```, ```useLocation``` pour la ```location```, et ```useRouteMatch``` pour le ```match```.



## Tester le routage avec React

### 8. Ce code utilise useParams, que nous n'avons encore jamais utilisé. A quoi sert-il ?
```useParams``` nous permet de récupérer des informations de l’url dans le navigateur.
Il renvoie un objet de paire clé/valeur des paramètres d’URL.



## Lien vers mini projet
https://codesandbox.io/s/interesting-leftpad-m0f08?file=/src/App.js

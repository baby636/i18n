## Classe : TouchBarLabel

> Créer un label dans la touch bar pour les applications native macOS

Processus : [Main](../tutorial/application-architecture.md#main-and-renderer-processes)

### `new TouchBarLabel(options)` *Experimental*

* `options` Objet 
  * `label` String (facultatif) - Texte à afficher.
  * `accessibilityLabel` String (optional) - A short description of the button for use by screenreaders like VoiceOver.
  * `textColor` String (facultatif) - Couleur hexadécimal du texte, c.-à-d. `#ABCDEF`.

When defining `accessibilityLabel`, ensure you have considered macOS [best practices](https://developer.apple.com/documentation/appkit/nsaccessibilitybutton/1524910-accessibilitylabel?language=objc).

### Propriétés d'instance

Les propriétés suivantes sont disponibles pour les instances de `TouchBarLabel` :

#### `touchBarLabel.label`

Un `String` représentant le texte du label actuel. Changer cette valeur met à jour immédiatement le label dans la touch bar.

#### `touchBarLabel.accessibilityLabel`

A `String` representing the description of the label to be read by a screen reader.

#### `touchBarLabel.textColor`

Un `String` représentant la couleur du texte du label actuel. Changer cette valeur met à jour immédiatement le label dans la touch bar.
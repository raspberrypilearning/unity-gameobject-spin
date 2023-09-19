![De spelweergave toont een hart GameObject dat rond zijn Y-as draait.](images/spinning-heart.gif)

Klik in het Inspector-venster voor het GameObject op 'Add Component' en kies 'New script'. Geef vervolgens je script een logische naam (bijvoorbeeld 'ItemController').

Dubbelklik op het nieuwe script om het te openen in de code editor.

Maak een variabele die de 'draaisnelheid' en code regelt om je Gameobject te laten draaien:

--- code ---
---
language: cs
---

    public float spinSpeed = 5.0f; 
    
    // Update is called once per frame
    void Update()
    {
        transform.Rotate(Vector3.forward * spinSpeed); //you can also spin backward, up, down, left and right
    }

--- /code ---

Je kunt roteren over de X, Y of Z assen door de richting in je code aan te passen:
+ Vector3.right / Vector3.left = Rotatie over de X-as
+ Vector3.up / Vector3.down = Rotatie over de Y-as
+ Vector3.forward / Vector3.back = Rotatie over de Z-as

**Tip:** Als je een 'Particle System' aan je GameObject hebt toegevoegd, verander de 'Simulatie Space' eigenschap in het Inspector venster naar `World` zodat het niet met je Gameobject mee draait.

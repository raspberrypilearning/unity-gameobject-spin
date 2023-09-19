![La vue Game montrant un GameObject tournant autour de son axe Y.](images/spinning-heart.gif)

Dans la fenêtre Inspector pour le GameObject, clique sur « Add Component » et choisis « New script », puis donne à ton script un nom approprié (par exemple « ItemController »).

Double-clique sur ton nouveau script pour l'ouvrir dans l'éditeur de code.

Crée une variable pour contrôler la « vitesserotation » et le code pour faire tourner ton GameObject :

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

Tu peux effectuer une rotation sur les axes X, Y ou Z en modifiant la direction dans ton code :
+ Vector3.right / Vector3.left = Rotation sur l'axe X
+ Vector3.up / Vector3.down = Rotation sur l'axe Y
+ Vector3.forward / Vector3.back = Rotation sur l'axe Z

**Astuce :** si tu as ajouté un « Particle System » à ton GameObject, modifie la propriété « Simulation Space » dans la fenêtre Inspector en `World` afin qu'il ne tourne pas avec ton GameObject.

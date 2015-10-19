Javascript
=========

https://www.dropbox.com/sh/n0p2lvar9v12lb4/AAC4_qm9w8-PliAlHyQ3E4yua?dl=0


Ejemplo 1:
----------

```javascript

<script>
    function recorrer () {
    var numeros = [23,20,50,63,24,32].sort();
    var x = parseInt(numeros.length)-1;
    var total = 0;

    for(i = 0;i<numeros.length;i++) {
        if(i == 0 || i== x) {
            alert("El número es "+numeros[i]);
        }
        else {

            alert("El número no es ni "+numeros[0]+" ni el número "+numeros[x]+" ("+numeros[i]+")");
        }
        total = total + numeros[i];
    }
    alert("La suma es: "+total)
    }
</script>

```
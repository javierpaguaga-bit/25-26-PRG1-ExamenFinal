El primer commit es el codigo fuerte original del problema

---

En el segundo commit "La linea 89 se quito porque no era necesaria para la validacion del formulario." se quito la siguiente linea de coodigo:

  int posicionArroba = -1;

ya que no formaba ninguna funcion

---

En el tercer commit "se ha cambiado n_regs por usuariosRegistrados para mayor claridad" fue hecho para ayudar a aclarar a futuros codificadores que hace la variable.

---

En el cuarto commit "se han simplificado las lineas 18 a 33 cambiando el uso de múltiples if por un switch." se intercambio lo siguiente:
```java
              if (opt.equals("2")) {
                System.out.println("Usuarios Registrados");
                if (usuariosRegistrados == 0) {
                    System.out.println("(No hay usuarios registrados)");
                }
                } else {
                    for(int i = 0; i < usuariosRegistrados
            ; i++) {
                        System.out.println((i+1) + ". Usuario: " + u_regs[i] + ", Email: " + e_regs[i]);
                                        System.out.println("Saliendo del sistema...");
                break;
            }
                }
            if (!opt.equals("1")) {
                System.out.println("Opcion no valida.");
                continue;
            }
```
Por un switch que va de la siguiente manera:
```java
                        switch(opt) {
                case "1" -> {
                }
                case "2" -> {
                    System.out.println("Usuarios Registrados:");
                    for (int i = 0; i < usuariosRegistrados; i++) {
                        System.out.println((i + 1) + ". " + u_regs[i] + " - " + e_regs[i]);
                    }
                    System.out.println("Saliendo del sistema...");
                    sc.close();
                    return;
                }
                default -> {
                    System.out.println("ERROR: Opcion no valida. Intente de nuevo.");
                    continue;
                }
                        }
```
a ser cambiado por un switch, la siguiente linea tampoco era necessaria:
```java
        sc.close();
```
---

En el quinto commit "organizando mejor el codigo en funcion del switch case." se organizo bien el codigo teniendo lo que estaba fuera del switch dentro del case 1, como deberia ser para ser claro.

---

En el sexto commit "se han cambiado u_regs y e_regs por nombres mas claros." por razon similares al tercero para ayudar a aclarar funciones de variables para futuro codificadores que lean o cambie el codigo.

---

En el septimo commit "se quito un comentario innecesario" se quito el comentario "//newline" por no ser necessario para entender la funcion del codigo.
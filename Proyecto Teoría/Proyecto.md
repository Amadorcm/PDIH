# Proyecto sobre librerías/paquetes/modulos de interfaces, en distintos lenguajes de programación #
---
# Java: Paquete Swing #

---
Codigo Ejemplo:
~~~ Java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class Interfaz extends JFrame {

private JDesktopPane desktopPane;
private JPanel panel;
private JLabel label;
private JTextField textField;
private JButton button;
private JComboBox<String> comboBox;
private JList<String> list;
private JCheckBox checkBox;

public Interfaz() {
super("Ejemplo de interfaz en Java");
setSize(800, 600);
setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
setLocationRelativeTo(null);

desktopPane = new JDesktopPane();
getContentPane().add(desktopPane, BorderLayout.CENTER);

panel = new JPanel();
panel.setLayout(null);
panel.setSize(250, 400);
panel.setLocation(20, 20);
desktopPane.add(panel);

label = new JLabel("Etiqueta");
label.setBounds(10, 10, 80, 20);
panel.add(label);

textField = new JTextField();
textField.setBounds(100, 10, 120, 20);
panel.add(textField);

button = new JButton("Botón");
button.setBounds(10, 50, 80, 20);
button.addActionListener(new ActionListener() {
public void actionPerformed(ActionEvent e) {
JOptionPane.showMessageDialog(null, "¡Hiciste clic en el botón!");
}
});
panel.add(button);

comboBox = new JComboBox<String>(new String[]{"Opción 1", "Opción 2", "Opción 3"});
comboBox.setBounds(100, 50, 120, 20);
panel.add(comboBox);

list = new JList<String>(new String[]{"Elemento 1", "Elemento 2", "Elemento 3"});
list.setBounds(10, 100, 210, 80);
panel.add(list);

checkBox = new JCheckBox("Checkbox");
checkBox.setBounds(10, 200, 100, 20);
panel.add(checkBox);

setVisible(true);
}

public static void main(String[] args) {
Interfaz interfaz = new Interfaz();
}

}
~~~
En este ejemplo, creamos una clase Interfaz que hereda de JFrame. En el constructor de la clase, creamos un JDesktopPane como contenedor principal, donde agregaremos los componentes de la interfaz.

Luego, creamos un JPanel para alojar los componentes de la interfaz. Utilizamos un layout nulo (null) para poder posicionar los componentes manualmente mediante el método setBounds(). Agregamos el panel al JDesktopPane.

Agregamos varios componentes al panel, incluyendo una etiqueta (JLabel), un campo de texto (JTextField), un botón (JButton), un combo box (JComboBox), una lista (JList) y un checkbox (JCheckBox). Modificamos las propiedades de cada componente mediante métodos como setBounds(), addActionListener() y new String[].

Finalmente, hacemos visible la ventana mediante el método setVisible(true).

---
# Python: Librería PyQt #
---
### Ventajas de usar PyQt ###
Flexibilidad de codificación - La programación GUI con Qt está diseñada alrededor del concepto de señales y slots para establecer comunicación entre objetos. Esto permite flexibilidad cuando se trata de eventos GUI y resulta en una base de código más fluida.

Más que un marco de trabajo - Qt utiliza una amplia gama de APIs de plataformas nativas con el propósito de redes, creación de bases de datos y mucho más. Ofrece acceso primario a ellos a través de una API única.

Varios componentes de la interfaz de usuario - Qt ofrece varios widgets, como botones o menús, todos ellos diseñados con una apariencia básica en todas las plataformas soportadas.

Varios recursos de aprendizaje: dado que PyQt es uno de los marcos de trabajo de interfaz de usuario más utilizados para Python, puede acceder fácilmente a una amplia gama de documentación.

---
Codigo Ejemplo:
~~~ Python


~~~
---
# Python: Librería Tkinter #

---

## Ventanas ##

- **Tk()**: Es la clase que crea las ventanas para añadir los widgets.
- **pack()**: Coloca los widgets en una posición de la ventana, que podremos cambiar a través de los correspondientes atributos.
- **mainloop()**: Inicia el bucle de mensajes, con esta función se monitorea la interacción del usuario a través del ratón o teclado con la aplicación, cuando se produzcaun evento recibiremos la notificacion correspondiente y podremos responder a dicho evento.

## Posicionamiento ##

### Place ###

Permite ubicar elementos indicando su posición (x,y).  

- Para valores **Absolutos**: `self.button.place(x=60, y=40, width=100, height=30)`
- Para valores **Relativos al padre (contenedor)**: `button.place(relx=0.1, rely=0.1, relwidth=0.5, relheight=0.5)`  
*Los argumentos aceptan valores entre 0 y 1*
---

### Ventajas de usar Tkinter ###
Disponible sin cargo para uso comercial.

Se presenta en la biblioteca Python subyacente.

La creación de ejecutables para las aplicaciones de Tkinter es más accesible ya que Tkinter está incluido en Python, y, como consecuencia, no viene con ninguna otra dependencia.

Simple de entender y dominar, ya que Tkinter es una librería limitada con una API simple, siendo la opción principal para crear interfaces gráficas de usuario rápidas para scripts Python.

---
Codigo Ejemplo:
~~~Python

~~~


---
# Referencias: #
Documentacion de Swing: https://download.java.net/java/early_access/loom/docs/api/java.desktop/javax/swing/package-summary.html

https://www3.uji.es/~belfern/Docencia/Presentaciones/ProgramacionAvanzada/Tema3/swing.html

Documentacion de PyQT: https://doc.qt.io/qtforpython-6/

Documentacion de Tk: https://docs.python.org/es/3/library/tk.html

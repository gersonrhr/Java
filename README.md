# Java
otras cosas

//Mensaje
JOptionPane.showMessageDialog(this, "Rut invalido","Error de Conexion",JOptionPane.WARNING_MESSAGE);


//Centrar Ventana
a.setLocationRelativeTo(null);

//visibilidad ventana
this.setVisible(false);


//Cantidad maxima de letras
 private void txtUsuarioKeyTyped(java.awt.event.KeyEvent evt) {                                    
  String Caracteres = txtUsuario.getText();
        if(Caracteres.length()>=10){
            evt.consume();
        }
    }  

//Solo numeros (RUT)
public void keyTyped(KeyEvent e) {
                char caracter = e.getKeyChar();
                if (((caracter < '0') || (caracter > '9')) && (caracter != '\b' ) && (caracter!='-') && (caracter!='k') ) {
                    e.consume(); // ignorar el evento de teclado
 }
}

//Evitar paste 
InputMap map2 = txtUsuario.getInputMap(txtUsuario.WHEN_FOCUSED);
map2.put(KeyStroke.getKeyStroke(KeyEvent.VK_V, Event.CTRL_MASK), "null"); 


//Maximo de letras
      String Caracteres = txtUsuario.getText();
        if(Caracteres.length()>=30){
            evt.consume();
        }

//Solo letras

char c=evt.getKeyChar();
if(Character.isDigit(c) || c =='.'|| c ==','|| c =='-'|| c =='´'|| c =='ç'||c =='`'||c =='+' ||c =='/'){
              getToolkit().beep();
              evt.consume() ;   
          }


//String a integer
Integer.parseInt();




















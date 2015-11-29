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

//Evitar paste (en Keypressed)
InputMap map2 = txtasd.getInputMap(txtasd.WHEN_FOCUSED);
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

// int a String:
String enteroString = Integer.toString(entero);


//Validacion de Fecha
public static boolean isFechaValida(String fecha) {
        try {
            SimpleDateFormat formatoFecha = new SimpleDateFormat("dd-MM-yyyy", Locale.getDefault());
            formatoFecha.setLenient(false);
            formatoFecha.parse(fecha);
        } catch (ParseException e) {
            return false;
        }
        return true;
    }


  public static boolean validarRut(String rut) {
 
        if (rut.indexOf("@")>0 ){
            return false;
        }
        boolean validacion = false;
        try {
            rut = rut.toUpperCase();
            rut = rut.replace(".", "");
            rut = rut.replace("-", "");
            int rutAux = Integer.parseInt(rut.substring(0, rut.length() - 1));
        
            char dv = rut.charAt(rut.length() - 1);
            if (rutAux==11111111){
                return false;
            }
            int m = 0, s = 1;
            for (; rutAux != 0; rutAux /= 10) {
                s = (s + rutAux % 10 * (9 - m++ % 6)) % 11;
            }
            if (dv == (char) (s != 0 ? s + 47 : 75)) {
                validacion = true;
            }
 
        } catch (java.lang.NumberFormatException e) {
        } catch (Exception e) {
        }
        return validacion;
    }











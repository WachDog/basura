# basura
<?xml version="1.0" encoding="UTF-8"?>

<?import javafx.geometry.Insets?>
<?import javafx.scene.control.Button?>
<?import javafx.scene.control.Label?>
<?import javafx.scene.layout.ColumnConstraints?>
<?import javafx.scene.layout.GridPane?>
<?import javafx.scene.layout.RowConstraints?>
<?import javafx.scene.layout.StackPane?>
<?import javafx.scene.layout.VBox?>
<?import javafx.scene.text.Font?>


<StackPane style="-fx-background-color: black;" xmlns="http://javafx.com/javafx/8.0.171" xmlns:fx="http://javafx.com/fxml/1" fx:controller="practica1.FXMLDocumentController">
   <children>
      <VBox alignment="CENTER" maxHeight="-Infinity" maxWidth="-Infinity" minHeight="-Infinity" minWidth="-Infinity" prefHeight="400.0" prefWidth="600.0">
         <children>
            <Label text="Tres en raya" textFill="#0084ff">
               <VBox.margin>
                  <Insets bottom="25.0" />
               </VBox.margin>
               <font>
                  <Font name="System Bold" size="36.0" />
               </font>
            </Label>
            <GridPane fx:id="grid" prefHeight="262.0" prefWidth="600.0">
              <columnConstraints>
                  <ColumnConstraints hgrow="SOMETIMES" minWidth="10.0" prefWidth="100.0" />
                <ColumnConstraints hgrow="SOMETIMES" minWidth="10.0" prefWidth="100.0" />
                <ColumnConstraints hgrow="SOMETIMES" minWidth="10.0" prefWidth="100.0" />
              </columnConstraints>
              <rowConstraints>
                <RowConstraints minHeight="10.0" prefHeight="30.0" vgrow="SOMETIMES" />
                <RowConstraints minHeight="10.0" prefHeight="30.0" vgrow="SOMETIMES" />
                <RowConstraints minHeight="10.0" prefHeight="30.0" vgrow="SOMETIMES" />
              </rowConstraints>
               <children>
                  <Button fx:id="v1" maxHeight="1.7976931348623157E308" maxWidth="1.7976931348623157E308" mnemonicParsing="false" onAction="#jugar" style="-fx-background-color: d7bc50;" textAlignment="CENTER">
                     <font>
                        <Font size="30.0" />
                     </font>
                  </Button>
                  <Button fx:id="v4" maxHeight="1.7976931348623157E308" maxWidth="1.7976931348623157E308" mnemonicParsing="false" onAction="#jugar" style="-fx-background-color: b5b2a4;" textAlignment="CENTER" GridPane.rowIndex="1">
                     <font>
                        <Font size="30.0" />
                     </font>
                  </Button>
                  <Button fx:id="v7" maxHeight="1.7976931348623157E308" maxWidth="1.7976931348623157E308" mnemonicParsing="false" onAction="#jugar" style="-fx-background-color: d7bc50;" textAlignment="CENTER" GridPane.rowIndex="2">
                     <font>
                        <Font size="30.0" />
                     </font>
                  </Button>
                  <Button fx:id="v2" maxHeight="1.7976931348623157E308" maxWidth="1.7976931348623157E308" mnemonicParsing="false" onAction="#jugar" style="-fx-background-color: b5b2a4;" textAlignment="CENTER" GridPane.columnIndex="1">
                     <font>
                        <Font size="30.0" />
                     </font>
                  </Button>
                  <Button fx:id="v5" maxHeight="1.7976931348623157E308" maxWidth="1.7976931348623157E308" mnemonicParsing="false" onAction="#jugar" style="-fx-background-color: d7bc50;" textAlignment="CENTER" GridPane.columnIndex="1" GridPane.rowIndex="1">
                     <font>
                        <Font size="30.0" />
                     </font>
                  </Button>
                  <Button fx:id="v8" maxHeight="1.7976931348623157E308" maxWidth="1.7976931348623157E308" mnemonicParsing="false" onAction="#jugar" style="-fx-background-color: b5b2a4;" textAlignment="CENTER" GridPane.columnIndex="1" GridPane.rowIndex="2">
                     <font>
                        <Font size="30.0" />
                     </font>
                  </Button>
                  <Button fx:id="v3" maxHeight="1.7976931348623157E308" maxWidth="1.7976931348623157E308" mnemonicParsing="false" onAction="#jugar" style="-fx-background-color: d7bc50;" textAlignment="CENTER" GridPane.columnIndex="2">
                     <font>
                        <Font size="30.0" />
                     </font>
                  </Button>
                  <Button fx:id="v6" maxHeight="1.7976931348623157E308" maxWidth="1.7976931348623157E308" mnemonicParsing="false" onAction="#jugar" style="-fx-background-color: b5b2a4;" textAlignment="CENTER" GridPane.columnIndex="2" GridPane.rowIndex="1">
                     <font>
                        <Font size="30.0" />
                     </font>
                  </Button>
                  <Button fx:id="v9" maxHeight="1.7976931348623157E308" maxWidth="1.7976931348623157E308" mnemonicParsing="false" onAction="#jugar" style="-fx-background-color: d7bc50;" textAlignment="CENTER" GridPane.columnIndex="2" GridPane.rowIndex="2">
                     <font>
                        <Font size="30.0" />
                     </font>
                  </Button>
               </children>
               <VBox.margin>
                  <Insets left="10.0" right="10.0" />
               </VBox.margin>
            </GridPane>
            <Button fx:id="reset" mnemonicParsing="false" onAction="#reiniciar" prefHeight="46.0" prefWidth="88.0" text="Reset" textFill="#0084ff">
               <opaqueInsets>
                  <Insets />
               </opaqueInsets>
               <VBox.margin>
                  <Insets bottom="10.0" top="25.0" />
               </VBox.margin>
               <font>
                  <Font size="15.0" />
               </font>
            </Button>
         </children>
      </VBox>
      <Label fx:id="ganador" alignment="CENTER" prefHeight="53.0" prefWidth="548.0" textFill="#00f556">
         <font>
            <Font name="System Bold" size="36.0" />
         </font>
      </Label>
   </children>
</StackPane>






    @FXML
    private Button v6;
    @FXML
    private Button v9;
    @FXML
    private Label ganador;
    
    private boolean esjugador1=true;
    private int jugadas=9;
    private String player1 ="Jugador X";
    private String player2 ="Jugador 0";
    
    @Override
    public void initialize(URL url, ResourceBundle rb) {
        ganador.setDisable(false);
        ganador.setVisible(false);
    }    

    @FXML
    private void jugar(ActionEvent event) {

        Button botoP = (Button) event.getSource();
        if (botoP.getText() == "") {
            if (esjugador1) {
                botoP.setText("X");
                combGanadoras(player1);
                esjugador1 = false;
                
            } else { //es jugador 2
                botoP.setText("O");
                combGanadoras(player2);
                esjugador1 = true;
            }
            jugadas--;
            if (jugadas == 0) {
                grid.setDisable(true);
            
            }
        }
    }
    
    @FXML
    private void reiniciar(ActionEvent event) {
        for (Iterator iterator = grid.getChildren().iterator(); iterator.hasNext();) {
            Button next = (Button) iterator.next();
            next.setText("");
        }
        grid.setDisable(false);
        //ganador.setText("");
        ganador.setDisable(false);
        ganador.setVisible(false);
        jugadas=9;
    }

    private boolean comb(Button n1, Button n2, Button n3){
        String s1 = n1.getText();
        String s2 = n2.getText();
        String s3 = n3.getText();
        return (s1.equals(s2) && s2.equals(s3) && !s1.equals(""));
    }
    private void combGanadoras(String g) {
        if (comb(v1,v2,v3) || comb(v4,v5,v6) || comb(v7,v8,v9) || comb(v1,v5,v9) || comb(v7,v5,v3) || comb(v1,v4,v7) || comb(v2,v5,v8) || comb(v3,v6,v9)){           
           
            ganador.setText("HA GUANYAT " + g);
            ganador.setDisable(true);
            ganador.setVisible(true);            
        }
    }

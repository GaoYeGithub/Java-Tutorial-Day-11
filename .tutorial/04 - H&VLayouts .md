# Vertical & Horizontal Layouts 

You can place this vertically/VBox. Or Horzontially/HBox.

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.layout.HBox;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

public class Main extends Application {

    @Override
    public void start(Stage primaryStage) {
        Button button1 = new Button("Button 1");
        Button button2 = new Button("Button 2");
        Button button3 = new Button("Button 3");

        // HBox arranges in a horizontal row
        HBox hbox = new HBox(10, button1, button2, button3); // 10 is the spacing between buttons
        
        // VBox arranges in a vertical column
        VBox vbox = new VBox(10, hbox, new Button("Button 4")); // Adding HBox and another button to VBox

        Scene scene = new Scene(vbox, 300, 200);

        primaryStage.setTitle("HBox and VBox Example");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}

```

And by default when you click something a blue border will appear

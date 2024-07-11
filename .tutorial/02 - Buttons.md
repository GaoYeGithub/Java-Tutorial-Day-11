# Adding a Button

Now let add some buttons.

👉 Type this line of code in `Main.java` and click `run`. 

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.Label;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

public class Main extends Application {

    @Override
    public void start(Stage primaryStage) {
        Label label = new Label("not clicked");
        Button button = new Button("Click here");

        // Action for the button click event
        button.setOnAction(e -> label.setText("clicked"));

        // layout pane that arranges its children in a vertical column
        VBox vbox = new VBox(10, label, button); // 10px is spacing between the label and button
        Scene scene = new Scene(vbox, 300, 200);

        primaryStage.setTitle("Button");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
```

And here it uses setOnAction to check if the button is press and what to do after it press here it send text to console.

<details><summary>💡Hint</summary>If you don't want to write .control just to javafx.scene* to import everything</details>

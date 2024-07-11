# Handling Events

## Button Click Events

Is somthing we done here a another example

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
        Label label = new Label("No button clicked yet");
        Button button = new Button("Click Me");

        // Set an action for the button click event
        button.setOnAction(e -> label.setText("Button clicked"));

        VBox vbox = new VBox(10, label, button); // 10px as spacing
        Scene scene = new Scene(vbox, 300, 200);

        primaryStage.setTitle("Handling Click Events");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
```

## Keyboard Events

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Label;
import javafx.scene.layout.StackPane;
import javafx.stage.Stage;

public class Main extends Application {

    @Override
    public void start(Stage primaryStage) {
        Label label = new Label("Press any key");
        StackPane root = new StackPane();
        root.getChildren().add(label);
        Scene scene = new Scene(root, 300, 200);

        // Set an action for key press events
        scene.setOnKeyPressed(event -> label.setText("Key Pressed: " + event.getCode()));

        primaryStage.setTitle("Keyboard Event");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
```







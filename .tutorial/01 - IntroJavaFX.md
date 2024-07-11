# Java Tutorial Day 11

## Introduction to JavaFX

Today we will be covering a framework for building GUIs in Java. creating and delivering desktop applications and rich Internet applications (RIAs). And today we will be contiuning from yesterday.
https://openjfx.io/

In order to start you need to use
https://replit.com/@replit/JavaFX-OpenJFX

👉 Copy this code into your coding editor in `Main.java` and see what happens when you hit `run`:

Let begin with make a simple GUI displaying hello world here it it is

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Label;
import javafx.scene.layout.StackPane;
import javafx.stage.Stage;

public class HelloWorld extends Application {

    @Override
    public void start(Stage primaryStage) {
        // label that display what inside the bracket
        Label helloLabel = new Label("Hello, World!");
        
        // StackPanesimple layout pane in a stack
        StackPane root = new StackPane();
        root.getChildren().add(helloLabel);

        // scene with the StackPane as the bottom and set its size x,y
        Scene scene = new Scene(root, 300, 200);

        // Set the title of window
        primaryStage.setTitle("Hello World");
        primaryStage.setScene(scene);
        
        // Display the primary stage
        primaryStage.show();
    }

    // main that launche the output
    public static void main(String[] args) {
        launch(args);
    }
}


```

Use stackPane, and scene to create the make Main Window, setTitle to create a Title, and label to display what you want to print
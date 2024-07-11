# Border Panes

Here are some possible placements for you stuff

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.layout.BorderPane;
import javafx.stage.Stage;

public class BorderPaneExample extends Application {

    @Override
    public void start(Stage primaryStage) {
        // BorderPane allows placement of elements in 5 different regions in 5 general location
        BorderPane borderPane = new BorderPane();

        borderPane.setTop(new Button("Top"));
        borderPane.setBottom(new Button("Bottom"));
        borderPane.setLeft(new Button("Left"));
        borderPane.setRight(new Button("Right"));
        borderPane.setCenter(new Button("Center"));

        Scene scene = new Scene(borderPane, 300, 200);

        primaryStage.setTitle("BorderPane");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
```


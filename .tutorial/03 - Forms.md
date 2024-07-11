# Forms

Yesterday we didn't really go over pratical applications today we will be build a login in form that ask for name and email.

```java
import javafx.application.Application;
import javafx.geometry.Insets;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.Label;
import javafx.scene.control.TextField;
import javafx.scene.layout.GridPane;
import javafx.stage.Stage;

public class Main extends Application {

    @Override
    public void start(Stage primaryStage) {
        Label nameLabel = new Label("Name:");
        TextField nameField = new TextField();

        Label emailLabel = new Label("Email:");
        TextField emailField = new TextField();

        // submit button and set action for it
        Button submitButton = new Button("Submit");
        submitButton.setOnAction(e -> {
            String name = nameField.getText();
            String email = emailField.getText();
            System.out.println("Name: " + name + ", Email: " + email);
        });

        // GridPane or rows and columns
        GridPane grid = new GridPane();
        grid.setPadding(new Insets(10, 10, 10, 10)); // Set padding 
        grid.setVgap(5); // vertical gap
        grid.setHgap(5); // horizontal gap

        // Add elements to specified column and row positions
        grid.add(nameLabel, 0, 0);
        grid.add(nameField, 1, 0);
        grid.add(emailLabel, 0, 1);
        grid.add(emailField, 1, 1);
        grid.add(submitButton, 1, 2);

        Scene scene = new Scene(grid, 300, 200);

        primaryStage.setTitle("Email Form");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}

```
Now you can create a simplue Gui and asking for name and email and receive it the consol
### You are on your way to being a coder in no time!

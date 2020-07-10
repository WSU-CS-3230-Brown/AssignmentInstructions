# Assignment 6 - String Operations GUI #

You should now have your number operations working in you GUI. Now it's time to add the String operations.

The application will have a 2nd screen or tab (probably use a TabPane) that will have a text field for inputing a list of strings and a button for executing the `palindrome` method. It will also output to either a new TextArea/Label or you may use the existing one if you'd like. Just like before make sure the user is unable to break anything with the UI or the inputs they enter. Validate the input. Also have some way for the user to clear the text in the TextField if they want. 

> IMPORTANT: Make sure you separate the controller methods into 2 classes, `NumberController` and `StringController`. This will require some refactoring.

See Example below of use of the `TabPane` with multiple fxml files. Note the `fx:controller` tags in each file. You will notice that there are actually 3 controllers. The MainController may or may not need any event handlers in it unless you want to share some elements between the tabs. Also note the `source` attribute in the `Tab` objects. This is how you'll reference your other fxml files.

## Main fxml file ##

```[fxml]
<?xml version="1.0" encoding="UTF-8"?>

<?import javafx.scene.control.*?>
<?import java.lang.*?>
<?import javafx.scene.layout.*?>
<AnchorPane maxHeight="-Infinity" maxWidth="-Infinity" minHeight="-Infinity" 
            minWidth="-Infinity" prefHeight="400.0" prefWidth="600.0" 
            xmlns="http://javafx.com/javafx/8" xmlns:fx="http://javafx.com/fxml/1" 
            fx:controller="com.github.ethanbrown3.cs3230.controllers.MainController">
   <children>
      <TabPane layoutX="127.0" layoutY="90.0" prefHeight="400.0" prefWidth="600.0" tabClosingPolicy="UNAVAILABLE" AnchorPane.bottomAnchor="0.0" AnchorPane.leftAnchor="0.0" AnchorPane.rightAnchor="0.0" AnchorPane.topAnchor="0.0">
        <tabs>
          <Tab text="Tab One Title">
               <content>
                  <fx:include fx:id="tabOne" source="TabOne.fxml" />
               </content>
          </Tab>
          <Tab text="Tab One Title">
               <content>
                  <fx:include fx:id="tabTwo" source="TabTwo.fxml" />
               </content></Tab>
        </tabs>
      </TabPane>
   </children>
</AnchorPane>
```

## tab one fxml file ##

```[fxml]
<?xml version="1.0" encoding="UTF-8"?>

<?import java.lang.*?>
<?import java.util.*?>
<?import javafx.scene.*?>
<?import javafx.scene.control.*?>
<?import javafx.scene.layout.*?>
<?import javafx.geometry.*?>

<VBox fx:id="loggerTab" prefHeight="444.0" prefWidth="491.0"
      xmlns="http://javafx.com/javafx/8" xmlns:fx="http://javafx.com/fxml/1" 
      fx:controller="com.github.ethanbrown3.cs3230.controllers.TabOneController">
    <children>
        ...
    </children>
</VBox>
```

## tab 2 fxml file ##

```[fxml]
<?xml version="1.0" encoding="UTF-8"?>

<?import java.lang.*?>
<?import java.util.*?>
<?import javafx.scene.*?>
<?import javafx.scene.control.*?>
<?import javafx.scene.layout.*?>
<?import javafx.geometry.*?>

<VBox fx:id="loggerTab" prefHeight="444.0" prefWidth="491.0"
      xmlns="http://javafx.com/javafx/8" xmlns:fx="http://javafx.com/fxml/1" 
      fx:controller="com.github.ethanbrown3.cs3230.controllers.TabTwoController">
    <children>
        ...
    </children>
</VBox>
```

I would recommend putting your controllers in a sub package of `com.github.youruser.cs3230.gui.controllers`. This will require that you add a new line to your `module-info.java` file (if you are not using java 8). Here's an example:

```[Java]
module cs3230Assignments {
        requires javafx.fxml;
        requires javafx.controls;

        opens com.github.ethanbrown3.cs3230.gui.controllers;
        opens com.github.ethanbrown3.cs3230.gui;
}
```

GPT-4 Prompt: "I need a tutorial to build a runelite plugin"

Creating a RuneLite plugin involves setting up a development environment, creating a new plugin project, and implementing the desired features. Here is a step-by-step tutorial to help you build your own RuneLite plugin:

## Step 1: Prerequisites

1. Install Java Development Kit (JDK) 16 or higher: https://adoptium.net/
2. Install an Integrated Development Environment (IDE) like IntelliJ IDEA: https://www.jetbrains.com/idea/download/
## Step 2: Clone and Import RuneLite Project

1. Open your terminal or command prompt and navigate to your desired workspace directory.
2. Clone the RuneLite GitHub repository:
```bash
git clone https://github.com/runelite/runelite.git
```
3. Open IntelliJ IDEA and import the cloned project by selecting "Open or Import" and selecting the "runelite" folder.
## Step 3: Configure the RuneLite Project

1. In IntelliJ IDEA, open the "Maven" tab on the right side of the window.
2. Click on the "Reload All Maven Projects" button (refresh icon) at the top of the Maven tab to load the project's dependencies.
3. Wait for the dependencies to download and for the project to build.
## Step 4: Create Your Plugin

1. In the "Project" tab on the left side, navigate to runelite-client/src/main/java/net/runelite/client/plugins/.
2. Create a new package for your plugin (e.g., myplugin) by right-clicking the "plugins" package, selecting "New" > "Package", and entering the package name.
3. In the newly created package, create a new Java class for your plugin (e.g., MyPlugin.java) by right-clicking the package, selecting "New" > "Java Class", and entering the class name.
4. Open MyPlugin.java and extend the Plugin class from net.runelite.client.plugins.Plugin. Also, add the @PluginDescriptor annotation with the necessary information (e.g., name, description, tags).

Example:

```java
package net.runelite.client.plugins.myplugin;

import net.runelite.client.plugins.Plugin;
import net.runelite.client.plugins.PluginDescriptor;

@PluginDescriptor(
    name = "My Plugin",
    description = "An example RuneLite plugin",
    tags = {"example", "tutorial"}
)
public class MyPlugin extends Plugin {
    // Your plugin implementation goes here
}
```
## Step 5: Implement Your Plugin Features

1. Override the startUp() and shutDown() methods to add any logic that should run when the plugin starts or stops, respectively.
2. Add any additional methods, classes, or logic necessary for your plugin's functionality. You can refer to existing RuneLite plugins for guidance.
## Step 6: Test Your Plugin

1. In IntelliJ IDEA, navigate to runelite-client/src/main/java/net/runelite/client/RuneLite.java.
2. Right-click the RuneLite.java file and select "Run 'RuneLite.main()'". This will build and launch the RuneLite client with your plugin.
3. Test your plugin by enabling it in the RuneLite client's settings panel.
## Step 7: Publish Your Plugin
If you want to share your plugin with others, you can publish it on GitHub or submit it as a pull request to the RuneLite project if you think it's valuable to the community. Remember to follow RuneLite's contribution guidelines if you want to submit a pull request.

That's it! You've successfully created a RuneLite plugin. Now you can expand your plugin with additional features or create new plugins to enhance your RuneScape experience.
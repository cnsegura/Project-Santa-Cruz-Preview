# QuickStart: Creating a Voice Assistant with the Project Santa Cruz Devkit

In this quickstart, you make your own voice assistant using the Project Santa Cruz Development Kit (DevKit) and [Speech services](https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/overview).

## Prerequisites

* Project Santa Cruz Development Kit with the Ear SoM connected.
* Speaker (not included in the devkit).
* [Onboarding](https://github.com/microsoft/Project-Santa-Cruz-Private-Preview/blob/main/user-guides/getting_started/azure-subscription-onboarding.md) complete.
* [OOBE](https://github.com/microsoft/Project-Santa-Cruz-Private-Preview/blob/main/user-guides/getting_started/oobe.md) complete.

## Devkit setup 

1. Connect speaker to your Ear SoM.
2. Connect the Ear SoM to your devkit.
3. Power on the devkit.
   * The 1st LED light on the Ear SoM will change to bright green to indicate Ear SoM was powered on. 
   *	The 2nd LED changes to blinking green to indicate Ear SOM is waiting for authentication.
4. Wait for the authentication process to complete. It can take up to 3 minutes.
5. Proceed to the next section when you see one of the following:
   * Both LED light turn off. This indicates that authentication is completed and devkit is not configured with a keyword.
   * Three bright blue light turn on. This indicates that authentication is completed and devkit is configured with a keyword.

**NOTE:** Reach out to your lead AED PM for support if your devkit cannot complete step 5.

## Project Santa Cruz in the Azure portal

The first step in creating a voice assistant is to navigate to the Project Santa Cruz in Azure portal.

1. Start your browser and go to the [Azure portal](https://go.microsoft.com/fwlink/?linkid=2135819).
2. Sign into your Azure account. 
3. Use the Search box at the top of the page, enter *Project Santa Cruz*.
4. In the list that appears, choose *Project Santa Cruz*. Your browser displays the Project Santa Cruz Overview page.

Alternatively, you can navigate directly to the [Project Santa Cruz Overview page](https://go.microsoft.com/fwlink/?linkid=2135819).

![Project Santa Cruz Portal](https://github.com/microsoft/Project-Santa-Cruz-Private-Preview/blob/main/user-guides/getting_started/getting_started_images/aed-portal-home-page.png)


## Create voice assistant using templates

You can build a voice assistant using available templates. The Hospitality template is available for the private preview. Healthcare is also scheduled to be released soon.

1. Open **Demos & Tutorials** tab. 
2. Click **Try out voice assistant templates** under **Speech tutorials and demos**.
3. Select IoT hub to which your device is connected from the **IoT hub** list.
4. Choose the device from the list.
5. Select one of the speech templates.
6. Click the **I agree to terms & conditions for this project.** checkbox.
7. Click **Create** button. The portal deploys the resource to the device.


![Project Santa Cruz Portal](https://github.com/microsoft/Project-Santa-Cruz-Private-Preview/blob/main/user-guides/getting_started/getting_started_images/aed-try-speech-themes.png)

8. Select the Azure subscription in the **Subscription** box.
9. Select the resource group to use from the **Resource group** list.
10. Enter name for the voice assistant. It will be used as a prefix to resource names.
11. Select the region to deploy resources to from the **Region** list.
12. Choose the pricing tier from the **Tier** list. (We recommend **Standard**).
13. Click the **Create** button. Resources for the voice assistant application will be deployed to your subscription. <br/>

**WARNING :** Do not close the pane until the portal finish deploying the resource. Closing the pane can result in unexpected behavior of voice assistant.
   
At this point, the portal displays the speech demo.

## Configure a keyword for your device

Next, you can add a keyword to your device so that you can activate it using voice. You can use prebuilt keywords and custom keywords created in [Speech Studio](https://speech.microsoft.com/).

1. Click on **change** link near **Custom keyword**.
2.	Select one of the available keywords. 

## Test out your voice assistant

Try any of the following commands to interact with your voice assistant. Always start with the keyword that you configured. For example - *Computer, turn on TV*.
* "Turn on lights."
* "Turn off lights."
* "Turn on TV."
* "Turn off TV."
* "Turn on AC."
* "Turn off AC."
* "Open blinds."
* "Close blinds."
* "Set temp to 75."

## Clean up resources

Follow these steps to clean up resources you deployed in this quickstart: 

1. From the Azure portal, select **Resource group** from the left menu.
2. Enter the resource group name (selected in step 9) in the **Filter by name** field.
3. Select the resource group from the list.
4. Open the resource group to view its resources.
5. There will be 6 resources with the name starting with prefix selected in step 10. Select each of them. 
6. Click **Delete** action in the top menu.
7. Confirm delete operation.
8. Press **Delete** to delete resources.

**WARNING:** This will remove any custom keywords you created in Speech Studio and voice assistant will no longer function. 

## Troubleshooting

### Project Santa Cruz is not available in the Azure portal

1. Verify the Azure portal link. For the Project Santa Cruz private preview you must use special link [Project Santa Cruz Overview page](https://go.microsoft.com/fwlink/?linkid=2135819).

### Voice Assistant was created but does not respond to commands

Check led lights on the Ear SOM. 
   * 3 bright blue lights indicate that voice assistant is ready and waiting for the keyword.
   * no lights when devkit is powered indicate that devkit completed initialization and needs to be configured.
   * any combination of green lights indicates that Ear SOM did not complete initialization. 

Read more about [Ear SOM led lights](https://github.com/microsoft/Project-Santa-Cruz-Preview/blob/main/user-guides/general/troubleshooting/ear_som_speech_module_troubleshooting.md#understanding-ear-som-led-indicators).
   
### Voice Assistant does not respond to a custom keyword created in Speech Studio

This might happen if the speech module is out of date. Follow these steps to update the speech module to the latest version.

1. Click on **Devices** in the left navigation menu.
2. Find your device in the list and click on it - the device window will open.
3. Open **Speech** tab.
4. Check module version.  
5. You will see the **Update** button if an update is available. 
6. Click on the **Update** button. usually it takes around 2-3 minutes to deply an updated version.

## Provide feedback

After completing the no-code speech solution, please provide feedback on your experience via this [questionnaire](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRzoJxrXKT0dEvfQyxsA0h8lUQU1YTDFUNkhBM005MFlYQkVQSFIxUURFRy4u). Your feedback will help us continue to fine-tune and improve the no-code speech experience.

For more information on Project Santa Cruz Quests and to provide feedback on other experiences, please visit the [test scenarios page](https://github.com/microsoft/Project-Santa-Cruz-Private-Preview/blob/main/user-guides/general/test-scenarios.md).

## Next Steps

Now that you have created a voice assistant, you could try creating a [Vision project](https://github.com/microsoft/Project-Santa-Cruz-Private-Preview/blob/main/user-guides/prototyping/create-nocode-vision.md).

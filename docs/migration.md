### 1.5.0

Whole flow of LunaID camera's now exposed through LunaID.allEvents(). User can subscribe to it to catch all events.  Or subscribe to specific events.
For example:

* LunaID.finishStates()

* LunaID.detectionCoordinates()

* LunaID.detectionErrors()

* LunaID.interactions()


###### Behaviour changes:
All callbacks was replaces with single native Flow api (CameraOverlayDelegateOut and CameraUIDelegate were removed).


- detection coordinates api changed:
was:
    CameraOverlayDelegateOut
became:
    LunaID.detectionCoordinates()
    

- CameraUIDelegate was removed:
was:
    CameraUIDelegate#bestShot
    CameraUIDelegate#canceled
    CameraUIDelegate#error
became:
    LunaID.finishStates()

- LunaID.showCamera() does not require CameraUIDelegate anymore.
    
- removed LunaID.unregisterListener()

- removed LunaID.popLastCameraState() and LunaID.getLastCameraState().

- LunaError and it's descendants are replaced with enum DetectionError.
was:
    LunaError.messageResId
became:
    DetectionError.messageResId

- Interaction parameters moved from LunaConfig. Now to setup blink interaction supply it's parameters to LunaID.showCamera().
was:
    LunaConfig.interactionEnabled
    LunaConfig.interactionTimeout
became:
    BlinkInteraction()


###### New:
LunaID.showCamera() now accepts list of interactions to run.





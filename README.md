# trackpad-is-too-damn-big

Trackpad Is Too Damn Big (TITDB) is a utility designed to customize trackpad behavior on Linux. TITDB creates a virtual trackpad device and forwards input events from the selected trackpad device to it while preventing other applications from receiving events from the original trackpad device and modifying the events to achieve the desired functionality. TITDB currently supports virtually reducing trackpad size in two different modes and one additional mode for printing input events without modifying them. TITDB has a very small memory and CPU footprint and is designed to be easily expandable for integrating new functionality in the future.

## Supported modes 

- **Print**: Print selected device properties and incoming events from the original device without modifying them.
- **Strict**: Completely disable designated areas of the trackpad based on specified percentages from the edges.
- **Flex**: Disable initial trackpad input from designated areas while allowing re-entry from valid areas and recognition of multitouch gestures. This ensures that the entire trackpad area remains usable and gestures are registered correctly without any restrictions.

## Troubleshooting
Because TITDB prevents other applications from receiving events from the original device, applications that specifically monitor the original device will not work as intended while TITDB is running. This can be easily resolved by configuring the applications to monitor the virtual device that TITDB creates instead of the original device.

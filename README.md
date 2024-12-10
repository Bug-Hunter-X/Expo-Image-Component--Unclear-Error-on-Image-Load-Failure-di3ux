# Expo Image Component: Unclear Error on Image Load Failure

This repository demonstrates a common but elusive bug when using the Expo `Image` component. The component fails to load an image without providing clear error messages, making debugging challenging. This issue occurs when the image URI is incorrect or inaccessible, or when network issues prevent image loading.

## Reproducing the Bug

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app using Expo Go or a similar Expo client.
4. Observe the error (or lack thereof) when trying to load the image.

## Solution

The solution involves robust error handling and checking the validity of the image URI before passing it to the `Image` component.  This includes implementing a `onError` prop to capture loading failures and ensuring the URI is correctly formatted and points to an accessible image.  We should also incorporate mechanisms for handling network requests, such as checking connectivity and providing feedback to the user.
# React Native

### [getting started with react native](https://facebook.github.io/react-native/docs/getting-started)

---

1. Name three Core Components of React Native and describe what they do.

- `<View>` :A container that supports layout with flexbox, style, some touch handling, and accessibility controls.

- `<Text>`:Displays, styles, and nests strings of text and even handles touch events.
- `<Image>`: Displays different types of images.

- `<ScrollView>`: A generic scrolling container that can contain multiple components and views.
- `<TextInput>`: Allows the user to enter text.

2. What problem does React Native solve (why call it native)?

   In Android development, you write views in Kotlin or Java; in iOS development, you use Swift or Objective-C. With React Native, you can invoke these views with JavaScript using React components. At runtime, React Native creates the corresponding Android and iOS views for those components. Because React Native components are backed by the same views as Android and iOS, React Native apps look, feel, and perform like any other apps. We call these platform-backed components Native Components.

3. What are the building blocks of a React Native app? How does that compare to a React app?

**React Native:**

- Components: Use mobile-specific components like `View` and `Text`.
- Native Modules: Access native features with platform-specific code.
- Styling: Style components with JavaScript.
- Navigation: Typically use React Navigation for app navigation.
- Performance: Optimize for mobile devices.

**React:**

- Components: Use web-specific components like `div` and `button`.
- Virtual DOM: Efficiently update the browser's DOM.
- Styling: Use CSS or CSS-in-JS libraries.
- Routing: Typically use React Router for web navigation.
- Platform: Focused on web development, not native mobile apps.

---

### [expo](https://expo.io/)

---

1. What solution does expo provide?

Expo provides a comprehensive solution for building React Native apps with simplified development and a range of built-in tools and libraries. It includes:

- **Development Environment:** Expo offers a development environment with a CLI (Command Line Interface) tool that streamlines React Native development.

- **Build and Deployment:** It simplifies the process of building and deploying React Native apps to both iOS and Android platforms.

- **Universal Modules:** Expo provides a set of universal modules for accessing native device features (e.g., camera, location, push notifications) without the need for writing native code.

- **Styling:** Expo allows you to style your app using JavaScript, similar to React Native, but it provides a simpler and more accessible way to manage styles.

- **Over-the-Air Updates:** Expo supports over-the-air updates, enabling you to update your app's JavaScript code without requiring users to download a new version from the app store.

- **Managed Workflow:** It offers a managed workflow that abstracts away some of the complexities of React Native development, making it easier for beginners to get started.

- **Expo Client App:** You can preview your app on real devices using the Expo Client app, which is available on both iOS and Android.

2. Expo tries to manage as much of the complexity of building apps as possible, which is why we call it the `Managed` workflow.

3. What is the difference between React Native and Expo?

   The main difference between React Native and Expo is that React Native is a framework for building mobile apps using JavaScript and native components, while Expo is a set of tools and libraries that simplifies and enhances the React Native development process. Here's a breakdown of their differences:

**React Native:**

- **Framework:** React Native is a JavaScript framework for building mobile apps. It provides the core infrastructure for creating cross-platform (iOS and Android) apps with a focus on flexibility and customization.

- **Freedom:** React Native offers more flexibility and control, allowing developers to write custom native code when needed. This makes it suitable for complex and highly customized applications.

- **Setup:** Setting up a React Native project from scratch involves configuring the development environment, which can be a bit complex for beginners.

- **Native Modules:** Developers need to write native modules in Java, Objective-C, or Swift to access certain device-specific features.

**Expo:**

- **Toolset:** Expo is a toolset and platform built around React Native. It provides a simplified and opinionated approach to building React Native apps.

- **Managed Workflow:** Expo offers a "Managed" workflow, which abstracts away much of the complexity involved in React Native development. This includes a set of pre-configured native modules and a simplified development environment.

- **Quick Start:** Expo provides a quick and easy way to start a new React Native project without the need for extensive configuration.

- **Universal Modules:** Expo includes a wide range of universal modules that allow developers to access native device features using JavaScript without writing native code.

- **Over-the-Air Updates:** Expo supports over-the-air updates, allowing you to update your app's JavaScript code without going through the app store approval process.

---

### [expo snack](https://snack.expo.io/)

---

1. Checkout this tool. What does snack allow you to do?

   Certainly! Here's your information in Markdown format with numbered points replaced by bullet points:

**Expo Snack**

- Expo Snack is a web-based platform that allows developers to quickly prototype, develop, and share React Native applications without the need for setting up a local development environment. It's part of the Expo framework, which is designed to simplify the process of building native mobile apps using JavaScript and React.

**Key Features and Benefits of Expo Snack**

- **Online Development**: With Expo Snack, you can write and test React Native code directly in your web browser. This eliminates the need for setting up development environments on your local machine, making it accessible and convenient for both beginners and experienced developers.

- **Live Preview**: You can see a live preview of your React Native app as you write code, which allows for rapid development and instant feedback. This feature accelerates the development process and makes it easier to spot and fix issues.

- **Shareable Projects**: Expo Snack allows you to share your projects with others by simply sharing a URL. This is useful for collaboration, troubleshooting, or getting feedback on your app from team members or the community.

- **Built-in Dependencies**: Expo Snack comes with a curated set of pre-installed libraries and dependencies commonly used in React Native development. This reduces the complexity of managing dependencies and configurations.

- **Support for Expo APIs**: Expo Snack supports a wide range of Expo APIs and components, making it easy to access native device features like camera, location, and sensors.

- **Easy Export**: When you're ready to move your project from Expo Snack to your local development environment or an Expo project, you can easily export the code and dependencies.

---

### [ejecting](https://docs.expo.io/versions/latest/expokit/eject)

---

1. What does “eject” mean within the context of Expo?

**eject**
The term "eject" was popularized by create-react-app, and it is used in Expo to describe leaving the cozy comfort of the standard Expo development environment, where you do not have to deal with build configuration or native code. When you "eject" from Expo, you have two choices:

- Eject to bare workflow, where you jump between workflows and move into the bare workflow, where you can continue to use Expo APIs but have access and full control over your native Android and iOS projects.
- Eject to ExpoKit, where you get the native projects along with ExpoKit. This option is deprecated and support for ExpoKit was removed after SDK 38.

2. When should you not eject?

- You should consider not ejecting from Expo's managed workflow when:

  - **Rapid Development**: For quick prototyping or MVPs, Expo's managed workflow offers fast development and validation.

  - **Limited Resources**: Smaller teams or solo developers may find it more efficient to stay in the managed workflow.

  - **Cross-Platform**: Expo simplifies cross-platform development with a unified codebase.

  - **Expo Services**: If you rely on Expo's services (OTA updates, push notifications), staying managed can save time.

  - **Few Custom Native Modules**: If your app doesn't need extensive custom native modules, managed workflow is often sufficient.

  - **Time and Cost Constraints**: Ejecting adds complexity; stick with managed workflow if time or budget is limited.

Ejecting should be considered when you need deep customization, extensive native code, or specific native library integrations.

3. Why might you choose to eject?

---

- You might choose to eject from Expo's managed workflow and move to the bare workflow in the following scenarios:

  - **Advanced Customization**: Ejecting provides greater control over your project's configuration, allowing you to customize it extensively, including integrating third-party native modules and modifying native code. This level of control is beneficial for complex projects with unique requirements.

  - **Access to Native Modules**: If your app requires access to specific device features or native modules that aren't available in Expo's managed workflow, ejecting allows you to integrate custom native code and libraries.

  - **Performance Optimization**: Ejecting provides opportunities for performance optimization, as you can fine-tune the native code and configurations to better suit your app's needs.

  - **Platform-Specific Development**: When you need to implement platform-specific functionality that can't be achieved through Expo's abstraction, ejecting allows you to write platform-specific code for iOS and Android.

  - **Direct Library Integration**: Ejecting makes it easier to integrate third-party native libraries and SDKs that may not be compatible with Expo's managed workflow.

  - **Full Control**: Ejecting grants you full control over your project's dependencies and build processes, which can be important if you have specific requirements or need to use non-standard tools.

  - **Complex Navigation**: If your app requires complex navigation patterns that aren't easily achievable with Expo's managed navigation solutions, you might consider ejecting to use a different navigation library.

  - **Offline Development**: Ejecting allows you to work offline without depending on Expo's servers for some development tasks, which can be important for certain projects.

  - **Long-Term Scalability**: For larger projects with long-term scalability needs, ejecting can be a strategic choice, as it provides more flexibility to adapt to changing requirements.

  - **Community or Team Expertise**: If you have team members or access to expertise in native development, ejecting may be a practical decision, as you can leverage their knowledge to build and maintain the app.

---

## [react native basics](https://facebook.github.io/react-native/docs/tutorial)

## [react native](https://facebook.github.io/react-native/)

## [Main Page](../README.md)

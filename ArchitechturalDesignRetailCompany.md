# Authors
- [Sherif Mansour](https://github.com/Sherif-Mansour)
- [Asenai Shiberim](https://github.com/AsenaiShiberim)

# 1. ADR - Native, web, or hybrid app

## Title
Selection of App Type: Native, Web, or Hybrid

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn

## Context
We are tasked with developing a mobile application for a retail company that allows customers to browse and purchase products, view order history, track deliveries, and participate in a loyalty program. The app must also support offline mode, push notifications, and internationalization.

## Decision
We have decided to develop a native mobile app.

## Consequence
Opting for native app development necessitates separate efforts for both iOS and Android platforms, potentially leading to higher initial development time and costs in comparison to web or hybrid approaches. Furthermore, maintaining two distinct codebases may demand additional resources over the long term. However, selecting a native approach enables us to capitalize on platform-specific features and enhance performance, ultimately delivering a smoother and more responsive user experience. Native development also offers robust support for crucial functionalities like offline mode and push notifications, which are integral requirements for our app's success. Despite the challenges associated with native development, the benefits in terms of performance and user experience outweigh the initial investment.

## Rationale
Given the imperative for high performance, seamless offline support, and seamless integration with device-specific features like push notifications, we're convinced that a native approach is the optimal choice for fulfilling the demands of the retail company's app. Despite potentially higher initial development costs and efforts compared to web or hybrid options, the long-term advantages of superior performance, user experience, and maintainability far outweigh these initial challenges. Moreover, native development empowers us to leverage platform-specific tools and libraries effectively, thereby augmenting the app's overall quality and functionality. In summary, prioritizing a native approach aligns seamlessly with our objectives of delivering an exceptional and feature-rich user experience while ensuring long-term scalability and maintainability.

---

# 2. ADR - UI Framework

## Title
Selection of UI Framework

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn

## Context
We are developing a mobile app for a retail company that allows customers to browse products, make purchases, view order history, track deliveries, and participate in a loyalty program. The app must support offline mode, push notifications, and internationalization. We need to decide on the appropriate UI framework to ensure a responsive, visually appealing, and consistent user interface across different devices and platforms.

## Decision
We have decided to utilize React Native for the UI framework.

## Consequence
Opting for React Native enables us to harness its cross-platform capabilities, facilitating the creation of a single codebase for both iOS and Android platforms. This consolidation reduces development time and cost significantly compared to managing separate UI codebases. React Native's component-based architecture further streamlines development by allowing efficient customization of UI components, ensuring a cohesive user experience throughout the app. Moreover, React Native benefits from a vibrant and expansive community, providing access to an extensive array of libraries, tools, and resources that expedite development and troubleshooting processes. However, it's essential to acknowledge potential limitations and performance considerations, especially concerning complex animations and interactions, when compared to fully native UI development. Despite these considerations, React Native presents a compelling solution for meeting our app's requirements while optimizing development efficiency and cost-effectiveness.

## Rationale
Considering the imperative for cross-platform compatibility, streamlined development, and an aesthetically pleasing user interface, React Native stands out as an ideal choice for the UI framework. Its capacity to simplify development processes while ensuring a native-like experience perfectly aligns with the demands of the retail company's app. Additionally, the robust community support and ecosystem surrounding React Native instill confidence in its sustainability and capability to tackle forthcoming challenges. Therefore, we are confident that embracing React Native as the UI framework will empower us to deliver a top-tier app that not only satisfies the requirements of the retail company but also exceeds the expectations of its clientele.

---

# 3. ADR - Backend Language

## Title
Selection of Backend Language

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn

## Context
We are tasked with developing a mobile app for a retail company that allows customers to browse products, make purchases, view order history, track deliveries, and participate in a loyalty program. The app must support offline mode, push notifications, and internationalization. In addition to the client-side development, we need to decide on the appropriate backend language to handle server-side logic, data management, and integrations with external services.

## Decision
We have decided to use Node.js as the backend language for the retail company's app.

## Consequence
By opting for Node.js, we can capitalize on its efficient handling of concurrent requests through its non-blocking I/O model and event-driven architecture. This capability ensures optimal performance and scalability, vital for accommodating a large user base. Additionally, Node.js boasts a vast ecosystem of modules and libraries available through npm (Node Package Manager), expediting development and facilitating seamless integration with third-party services like payment gateways, analytics tools, and push notification services. However, it's important to note that Node.js may not be the most suitable option for CPU-intensive tasks or heavy computational operations due to its single-threaded nature. Furthermore, while JavaScript is familiar to frontend developers, there may be a learning curve for those less experienced in server-side development. Despite these considerations, the benefits of Node.js outweigh the potential challenges, making it an advantageous choice for powering the backend of the retail company's app.

## Rationale
Given the imperative for scalability, performance, and developer efficiency, Node.js presents itself as a fitting candidate for the backend language. Its asynchronous and event-driven architecture harmonizes seamlessly with the demands of managing numerous concurrent requests and real-time interactions commonly encountered in mobile apps. Moreover, the expansive npm ecosystem furnishes a plethora of modules and tools, facilitating swift development and seamless integration of fundamental backend functionalities. Overall, embracing Node.js as the backend language equips us to construct a resilient and scalable backend infrastructure adept at supporting the retail company's app comprehensively. This strategic decision positions us favorably to meet the app's evolving needs while fostering continued growth and innovation.

---

# 4. ADR - Permissions

## Title
Permissions Management

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn 

## Context
We are developing a mobile app for a retail company that enables customers to browse products, make purchases, view order history, track deliveries, and participate in a loyalty program. Additionally, the app supports offline mode, push notifications, and internationalization. To ensure data security, privacy, and proper access control, we need to define the permissions architecture for managing user permissions within the app.

## Decision
We have decided to implement a role-based access control (RBAC) system for managing permissions in the app.

## Consequence
By implementing an RBAC system, we establish clear user roles (such as customer, administrator, and delivery personnel) and allocate precise permissions to each role, aligning with their responsibilities and access necessities. This strategy affords granularity in access control, guaranteeing that users can only access features and data pertinent to their role, thereby upholding data security and integrity. However, the design and implementation of an RBAC system necessitate meticulous planning, considering factors such as role hierarchy, permission inheritance, and role assignment mechanisms. Additionally, ongoing maintenance of RBAC policies may be required to accommodate app evolution and changes in user roles.

## Rationale
RBAC stands as a widely embraced access control model, esteemed for its flexibility, scalability, and streamlined management, rendering it an ideal fit for permissions management within the retail company's app. Through the delineation of explicit roles and permissions, we can adeptly enforce access control policies, mitigating the peril of unauthorized access and ensuring alignment with data protection regulations. Moreover, RBAC simplifies user management processes such as onboarding, offboarding, and role assignment, bolstering administrative efficiency and minimizing error likelihood. In essence, the adoption of an RBAC system resonates with the app's imperatives for secure and regulated access to data and functionalities, thus positioning it as a judicious architectural decision.

---

# 5. ADR - Data Storage

## Title
Data Storage Architecture

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn

## Context
We are developing a mobile app for a retail company, enabling customers to browse products, make purchases, view order history, track deliveries, and participate in a loyalty program. Additionally, the app supports offline mode, push notifications, and internationalization. To effectively manage and store the app's data, including user information, product catalogs, order details, and loyalty program data, we need to decide on the appropriate data storage architecture.

## Decision
We have decided to implement a combination of relational and NoSQL databases for the retail company's app.

## Consequence
By blending relational and NoSQL databases, we can harness the best of both worlds to cater to the diverse data storage needs of our app. Relational databases like MySQL are perfect for structured data, ensuring data integrity and handling complex queries—ideal for storing transactional information such as orders and user profiles. Meanwhile, NoSQL databases like MongoDB shine in managing unstructured or semi-structured data, offering scalability and supporting flexible data models, which are great for things like product catalogs and real-time data. However, managing multiple databases introduces complexities in data synchronization, consistency, and transactions, requiring careful planning and integration strategies. It's crucial to ensure data consistency and integrity across different database systems by implementing suitable data synchronization mechanisms.

## Rationale
We've chosen to blend relational and NoSQL databases to address the varied data storage needs of our retail company's app while ensuring scalability, performance, and data consistency. Relational databases offer robustness and adhere to ACID (Atomicity, Consistency, Isolation, Durability) principles, making them ideal for managing important transactional data. Meanwhile, NoSQL databases provide flexibility, scalability, and support for semi-structured data, perfectly suited for dynamic and rapidly changing datasets. By combining these approaches, we strike a balance that optimizes both data storage and retrieval performance, allowing us to adapt to the evolving demands of our app's data requirements.

---

# 6. ADR - Authentication and Authorization Framework

## Title
Selection of Authentication and Authorization Framework

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn

## Context
We are developing a mobile app for a retail company that allows customers to browse products, make purchases, view order history, track deliveries, and participate in a loyalty program. Additionally, the app supports offline mode, push notifications, and internationalization. To ensure data security and proper access control, we need to decide on the appropriate authentication and authorization framework for managing user authentication and permissions within the app.

## Decision
We have decided to implement JSON Web Tokens (JWT) for authentication and role-based access control (RBAC) for authorization in the retail company's app.

## Consequence
Implementing JWT for authentication enhances our app's security by securely transmitting user credentials using digitally signed tokens, reducing the risk of unauthorized access or data tampering. JWTs also offer stateless authentication, promoting scalability and minimizing server-side storage needs. However, we must carefully consider security best practices, token expiration policies, and validation mechanisms to guard against potential vulnerabilities like token replay attacks. Incorporating RBAC for authorization allows us to define specific user roles (e.g., customer, administrator, delivery personnel) and assign tailored permissions based on their responsibilities and access needs. This granular approach ensures users only access relevant features and data, upholding data security and integrity. However, designing and implementing an RBAC system requires thorough planning, considering factors like role hierarchy, permission inheritance, and role assignment methods. Additionally, RBAC policies may need periodic updates to adapt to app changes and evolving user roles.

## Rationale
We've chosen to implement JWT for authentication and RBAC for authorization in our retail company's app to prioritize data security, scalability, and effective access control. JWTs offer a secure and streamlined method for authenticating users and transmitting authentication tokens, while RBAC provides a versatile and detailed approach to defining and enforcing access control policies. By adopting these standardized authentication and authorization frameworks, we're able to establish strong security measures and elevate the overall integrity and reliability of the app.

---

# 7. ADR - Push Notification Service Provider

## Title
Selection of Push Notification Service Provider

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn

## Context
We are developing a mobile app for a retail company that enables customers to browse products, make purchases, view order history, track deliveries, and participate in a loyalty program. Additionally, the app supports offline mode, push notifications, and internationalization. To effectively engage users and provide timely updates, we need to decide on the appropriate push notification service provider for managing push notifications within the app.

## Decision
We have decided to integrate Firebase Cloud Messaging (FCM) as the push notification service provider for the retail company's app.

## Consequence
Opting for Firebase Cloud Messaging (FCM) allows us to tap into its broad support for both iOS and Android platforms, reaching a diverse audience of mobile users. FCM comes packed with a robust feature set, including message targeting, personalization, analytics, and support for rich media notifications, empowering us to deliver captivating and pertinent push notifications to users. Furthermore, FCM ensures dependable message delivery, scalable infrastructure, and real-time monitoring capabilities, guaranteeing optimal performance and availability even during peak usage periods. However, integrating FCM may necessitate additional development effort and expertise, especially in configuring and managing push notification campaigns, as well as handling device registration and token management.

## Rationale
We've opted to integrate Firebase Cloud Messaging (FCM) as our push notification service provider due to its robust feature set, cross-platform support, reliability, and scalability. FCM provides a seamless solution for managing push notifications across both iOS and Android platforms, streamlining development and ensuring a consistent user experience across devices. Additionally, FCM's extensive features and analytics capabilities empower us to create targeted and personalized push notification campaigns, which can drive user engagement and retention. Overall, integrating FCM aligns perfectly with the needs of our retail company's app, enabling us to deliver timely and relevant push notifications to enhance the overall user experience.

---

# 8. ADR - Analytics Tool or Service

## Title
Selection of Analytics Tool or Service

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn

## Context
We are developing a mobile app for a retail company that enables customers to browse products, make purchases, view order history, track deliveries, and participate in a loyalty program. Additionally, the app supports offline mode, push notifications, and internationalization. To gain insights into user behavior, track app performance, and improve the overall user experience, we need to decide on the appropriate analytics tool or service for collecting and analyzing app usage data.

## Decision
We have decided to integrate Google Analytics for Firebase as the analytics tool for the retail company's app.

## Consequence
By incorporating Google Analytics for Firebase, we can harness its powerful analytics features, such as event tracking, user segmentation, conversion tracking, and funnel analysis, to gain valuable insights into user behavior and app performance. Google Analytics for Firebase offers an intuitive dashboard and reporting interface, making it easy to visualize and analyze app usage data effectively. Moreover, Firebase's seamless integration with other Google services, like Google Ads and Google Cloud Platform, enables seamless data sharing and cross-platform analysis, bolstering the app's marketing and business intelligence capabilities. However, integrating Google Analytics for Firebase may require additional development effort and expertise, especially in setting up custom events and configuring advanced analytics features. Additionally, ensuring compliance with data privacy regulations, such as GDPR and CCPA, is crucial when collecting and processing user data through Google Analytics for Firebase. It's essential to prioritize user privacy and adhere to regulatory requirements throughout the integration process.

## Rationale
The decision to integrate Google Analytics for Firebase as our analytics tool stems from its comprehensive feature set, seamless integration capabilities, and user-friendly interface. Google Analytics for Firebase provides a powerful solution for collecting, analyzing, and visualizing app usage data, allowing us to make informed decisions and enhance the app's performance and user experience. Additionally, Firebase's robust infrastructure and scalability ensure reliable data collection and analysis, accommodating our app's growth without compromising data integrity. Overall, integrating Google Analytics for Firebase aligns perfectly with the needs of our retail company's app, empowering us to drive continuous improvement and innovation through data-driven insights.

---

# 9. ADR - Image Storage Solution & Optimization Techniques

## Title
Selection of Image Storage Solution & Optimization Techniques

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn

## Context
We are developing a mobile app for a retail company that enables customers to browse products, make purchases, view order history, track deliveries, and participate in a loyalty program. Additionally, the app supports offline mode, push notifications, and internationalization. To ensure optimal performance and user experience when displaying product images, we need to decide on the appropriate image storage solution and optimization techniques for managing and serving images within the app.

## Decision
We have decided to use a combination of cloud storage services and image optimization techniques for managing and serving images in the retail company's app.

## Consequence
By harnessing cloud storage services like Amazon S3, Google Cloud Storage, or Firebase Storage, we can efficiently store and deliver images, ensuring top-tier availability, scalability, and reliability. These services provide robust storage solutions with built-in redundancy and data replication, greatly reducing the risk of data loss or downtime. Moreover, they leverage content delivery networks (CDNs) for swift and dependable content delivery, guaranteeing minimal latency and high throughput for users worldwide. Integrating image optimization techniques such as caching, lazy loading, and compression further enhances performance and load times while reducing bandwidth usage. This means we can trim image file sizes and improve app performance significantly. However, implementing these techniques may necessitate additional development expertise, especially in fine-tuning caching strategies, compression algorithms, and lazy loading mechanisms to ensure optimal results.

## Rationale
We've opted to combine cloud storage services with image optimization techniques to prioritize optimal performance, scalability, and cost-effectiveness in managing and serving images within the app. Cloud storage services offer a dependable and scalable solution for storing and delivering images, while image optimization techniques help us reduce bandwidth usage and enhance app performance. By leveraging both approaches, we can provide users with a seamless and visually appealing experience while keeping infrastructure costs and operational overhead to a minimum. Overall, this strategy aligns perfectly with the needs of our retail company's app and allows us to efficiently manage and serve images to users worldwide.

---

# 10. ADR - Location Tracking and Geolocation Services

## Title
Selection of Location Tracking and Geolocation Services

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn

## Context
We are developing a mobile app for a retail company that enables customers to browse products, make purchases, view order history, track deliveries, and participate in a loyalty program. Additionally, the app supports offline mode, push notifications, and internationalization. To provide accurate location-based features such as restaurant recommendations, estimated delivery times, and order tracking, we need to decide on the appropriate approach for location tracking and geolocation services within the app.

## Decision
We have decided to utilize the native geolocation APIs provided by the mobile operating systems (e.g., Core Location for iOS and Location Services for Android) for location tracking and geolocation services in the retail company's app.

## Consequence
Utilizing native geolocation APIs grants us access to precise and dependable device-level location data, seamlessly integrating with our app's functionalities. These APIs offer a wide array of location-based services, including GPS positioning, geocoding, and proximity detection, enabling us to implement features such as real-time location tracking and geofencing. Moreover, native geolocation APIs come equipped with built-in privacy controls and consent mechanisms, ensuring compliance with data protection regulations and respecting user privacy. However, relying solely on native geolocation APIs may pose challenges in terms of interoperability and portability across different mobile platforms, necessitating platform-specific implementation and testing efforts. Despite these considerations, the benefits of accuracy, reliability, and regulatory compliance make native geolocation APIs the preferred choice for our app's location-based functionalities.

## Rationale
We've decided to utilize native geolocation APIs for location tracking and geolocation services due to their inherent advantages in accuracy, reliability, and seamless integration with mobile operating systems. These APIs grant access to device-level location data with exceptional precision and efficiency, allowing us to deliver highly accurate and contextually relevant location-based features to our users. Additionally, native geolocation APIs come with robust privacy controls and user consent mechanisms, ensuring compliance with data protection regulations and fostering trust and transparency with our users. Overall, leveraging native geolocation APIs perfectly aligns with the requirements of our retail company's app, enabling us to provide a seamless and personalized user experience based on real-time location data while upholding user privacy and regulatory compliance.

---

# 11. ADR - Payment Gateway Integration

## Title
Selection of Payment Gateway Integration

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn

## Context
We are developing a mobile app for a retail company that allows customers to browse products, make purchases, view order history, track deliveries, and participate in a loyalty program. Additionally, the app supports offline mode, push notifications, and internationalization. To facilitate secure and convenient transactions for customers, we need to decide on the appropriate payment gateway or combination of gateways to integrate with the app.

## Decision
We have decided to integrate Stripe as the primary payment gateway for the retail company's app.

## Consequence
Integrating Stripe as our primary payment gateway offers numerous benefits, including its robust payment processing infrastructure, advanced security features, and extensive support for various payment methods and currencies. With Stripe, we can provide customers with a seamless checkout experience, accommodating card payments, digital wallets, and alternative payment methods for added convenience and flexibility. Moreover, Stripe's comprehensive fraud prevention tools, including machine learning-based fraud detection and chargeback protection, help safeguard against fraudulent transactions and ensure transaction security. Additionally, Stripe provides detailed analytics and reporting features, empowering us to monitor transaction performance, analyze payment trends, and optimize the checkout process for improved conversion rates. However, integrating Stripe may require additional development effort and expertise, particularly in configuring payment flows, handling payment callbacks, and implementing PCI DSS compliance requirements to ensure data security and regulatory compliance. Despite these considerations, the advantages of Stripe make it an ideal choice for our payment processing needs.

## Rationale
The decision to integrate Stripe as our primary payment gateway is motivated by its stellar reputation as a top-tier payment processor, its extensive feature set, and its steadfast commitment to security and compliance. With Stripe, we gain access to a reliable and scalable payment processing solution that supports a wide array of payment methods and currencies, catering to the global scope of our retail app. Moreover, Stripe's developer-friendly APIs, comprehensive documentation, and robust support resources streamline the integration process, allowing us to bring our app to market more quickly. Overall, integrating Stripe perfectly aligns with the needs of our retail app, enabling us to provide customers with a secure, seamless, and hassle-free payment experience.

---

# 12. ADR - Localization Framework or Libraries

## Title
Selection of Localization Framework or Libraries

## Status
**Proposed** / Accepted / Rejected / Implemented / Deferred / Withdrawn

## Context
We are developing a mobile app for a retail company that allows customers to browse products, make purchases, view order history, track deliveries, and participate in a loyalty program. Additionally, the app supports offline mode, push notifications, and internationalization. To support multiple languages and adapt to various cultural preferences, we need to decide on the appropriate localization framework or libraries for implementing localization techniques within the app.

## Decision
We have decided to utilize the i18next library for implementing localization in the retail company's app.

## Consequence
By integrating the i18next library, we unlock its powerful localization capabilities, offering support for multiple languages, dynamic language switching, interpolation, pluralization, and formatting. This library provides a flexible and user-friendly approach to managing localization resources, enabling efficient organization and customization of language files tailored to our app's needs. i18next comes with comprehensive documentation, tutorials, and examples, facilitating easy adoption and troubleshooting for developers. Additionally, its active maintenance and vibrant community ensure ongoing support and updates for the library. However, integrating i18next may entail additional development effort and expertise, especially in configuring localization resources, managing translation workflows, and addressing challenges related to text expansion and RTL languages. Despite these considerations, i18next empowers us to create a globally accessible app with seamless multilingual support.

## Rationale
We've opted to utilize the i18next library for localization due to its versatility, flexibility, and robust feature set, all of which seamlessly align with the needs of our retail app. i18next provides a comprehensive solution for managing localization resources and implementing localization workflows, empowering us to deliver a culturally relevant user experience to our diverse global audience. Moreover, i18next's active community and extensive documentation resources offer invaluable support and guidance throughout the localization process, enabling us to efficiently tackle any challenges or issues that may arise. Overall, integrating i18next perfectly aligns with the objectives of our retail app, allowing us to effectively cater to multiple languages and cultural preferences while ensuring a seamless user experience.

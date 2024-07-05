# Unit 2: Creating Visual Representation

## Visualization Reference Model

It is a conceptual model that describe the different components involved in data visualization and act as a guide to design and development of visualization system to help users to understand to interpret the result and use visualization in effective way. It helps data analysts, designers and stakeholders to ensure that the visualizations are clear informative and aligned with the goals of the project. It provides set of guidelines and design principle that can be used to create visually appealing and informative visualization eccentrics like charts, graphs, line charts, scatter plot etc. Following are the common element that a visual reference model includes:

- **Data**: Represents the elements that are being visualized and can be structure or unstructured or quantitative or qualitative.

- **Interaction**: It shows how user can interact with visualization or in what ways user can interact. This includes the features like zooming, panning, tooltips and filtering.

- **Color**: Specify a consistent color to use in visualization which makes the output more visually appealing. This includes guidelines for primary colors, accent color, how to use color to represent different data categories or values.

- **Evaluation**: This includes the way that the effectiveness of the visualization is measured as well as the way the visualization is tailored to the needs of the users.

- **Layout**: Determine the overall layout of the visualization including the placement of axes, legends and data element. This includes margins, padding and spacing to create a balanced composition.

- **Data Encoding**: Define how variables should be mapped to visual properties such as position, size, shape and color. It ensures that the encoding choices align with the goals of the visualization and make it easy for viewer to interpret the data.

- **Annotations and Labels**: Specify guidelines for adding annotations, titles and labels to clarify and contextualize the data. Annotation can include trend line, labels or text.

- **Legends and Scales**: Define how legends and scales should be presented when using color, size or other visual encodings. Legends helps to interpret the visualization.

- **Consistency**: This includes consistent use of colors, fonts and design element. It helps to maintain minimum deviation between actual result and result from visualization tools.

## Visual Mapping

It refers to the process of assigning visual attributes and properties to data elements in order to represent specific information and patterns effectively. That is, it is the process of representing data in visual perceptive using different visualization eccentrics like map, chart, graph etc. It is a crucial step to transform raw data into meaningful and informative visual representation and involves thoughtful decisions about encoding data using visual variables to create clear and insightful visualization. It helps viewer to interpret data quickly and accurately by understanding human perception and cognition. It includes making decision about encoding data variables, using visual channels such as position, size, color, shape and texture. When choosing a visual mapping technique, following factor should be considered:

- The type of data that are to be visualized.
- The message to be communicate with viewer.
- The target viewer.
- The available tools and resources.

Some of the examples of visual mappings are bar chars that uses bars to represent different values and comparison between them, line charts to show trends or change over time, scatter plot that uses dot to show correlation between variables, pie chart that uses slices of pie to show relative proportion of different values, map that uses geographic features to show relation between different data points. The choice of mapping depends on the data type, the message to be conveyed and the target audience. Following are the key aspect of visual mapping in data visualization:

- **Visual Variables**: Visual Variables are the attributes that can be used to encode data like position (x axis and y axis to create scatter plots, bar charts etc.), size (represents data value by varying the size of graphical elements like points, bar etc.), color (to distinguish categories, numerical values or emphasize specific data points), shape (circle, square, triangles etc. to encode categories or data attributes), texture (to differentiate data elements when color is not suitable or to add additional encoding), opacity/transparency (to show overlapping data points or emphasize specific data regions).

- **Mapping Data Types**: Data types like nominal, ordinal, interval ratio require different visual mappings. Nominal data may be mapped using distinct colors or shapes while ordinal data might use gradients of color or size to indicate order.

- **Data Attributes**: Data Attributes includes specific attributes like quantitative, categorical, temporal or spatial which may require different mapping strategy.

- **Scale and Range**: Determine the range of values for each visual variables in which different color can be mapped using continuous gradient or discrete color palette.

- **Normalization**: While comparing multiple data attributes or datasets it is necessary to normalize or standardize the data to ensure fair and meaningful visual comparisons.

- **Interactivity**: This includes effects like zooming, filtering or highlighting data points through user interaction.

- **Accessibility**: Ensures that the chosen visual mappings are accessible to all users and should provide alternative text for visual elements and consider using proper color palettes.

## Visual Analytics

It is an approach to data analysis that combines interactive data visualization with advance analytical techniques which aims to helps users gain insight from complex data by using visualization, statistical and human cognition. It combines data visualization, data mining and interactive techniques to helps users explore and understand large and complex datasets. It is a tool for gaining effective insights from data that is difficult or impossible to gain from traditional methods. Therefore, visual analytics help users to explore, interact with data and to explore relationships and patterns. Visual analytics is widely used in various domains including business intelligence, healthcare, finance and scientific research etc. Some of the tools used for visual analytics are power bi, tableau, ggplot, matplotlib,etc. Following are the advantage of visual analytics in data visualization:

- Help user to understand complex data more easily.
- Help user to identify patterns and trends that are difficult to analyze from spreadsheet or table.
- Can be used to share data with others and to collaborate on analysis.
- Helps to drill down on specific areas of interest.

**Visual analytics involves several key components and principles:**

1. **Interactive Visualizations:** Includes filter, zoom, drill down and manipulate visual representations to uncover patterns, trends and outliers.
2. **Data Integration:** Visual analytics involves integration of data from multiple sources and formats ie. includes structured data from databases, unstructured data from text sources and real time data which enable more comprehensive analysis.
3. **Visual Data Exploration:** Includes charts, graphs, maps and dashboard to visually explore complex data which helps users to understand and interpret such complex data and their relationship. It includes bar chart, line chart, scatter plots and geographic maps.
4. **Data Transformation:** Visual analytics tools provide data transformation capabilities, including data cleaning, transformation capabilities, data cleaning to prepare data for analysis.
5. **Data Security and Privacy:** For the sensitive data, visual analytics platforms often incorporate security and privacy features to ensure data protection and compliance with regulation.
6. **Customization:** Using visual analytics tools users can customize the visualizations to suit their specific needs which may includes adjusting color, fonts and different layouts.

### Importance of Visual Analytics

- **Enhanced Data Understanding**: Visual analytics involves in representing complex data in visual form that allows users to see patterns, trend and outlines which may not be seen in raw data or text-based reports.
- **Effective Communication**: Visualization conveys information quickly and efficiently which enable clear and concise communication of data finding to users. Visual analytics helps to bridge the gap between data experts and non-experts.
- **Decision Making**: Visual analytics empowers decision makers to base their choices on data driven insights rather that intuition or evidence which leads to more informed and strategic decision.
- **Real Time Monitoring**: Visual analytics supports different tool for time series data which enables organization to respond quickly to changing conditions and make timely intervention or adjustment.
- **Pattern Recognition**: Our visual perception is more suited for recognizing different patterns and anomalies. Visual analytics helps to simplify this character by allowing users to identify irregularities, trends and outliers more effectively than with traditional data analysis methods.

## Design of Visualization Applications

It involves planning and consideration of various aspects likes user needs, data complexity, interactivity and usability. Throughout the design and development process, it is necessary to consider involving users and stakeholder for feedback and validation. Collaboration and user centered design are essential for creating a successfully visualization application that meets both functional and user experience requirements. Following are the key design principles:

- Define objectives and users' goals.
- Understand audience
- Select proper visualization: Choose right types of visualization eccentrics for data like bar chart, line chart, scatter plot based on nature of data and user requirements.
- Plan data preparations: Ensure data is cleaned, structured and stored in a way that is suitable for visualization. Use data transformation and aggregation before visualizing data
- Visual Consistency: Maintain visual consistence across application ie. use appropriate and uniform color scheme, typography and layout.
- Testing and Iterations: Conduct testing with real users to identify points and areas for improvement and iteratively refine the design based on user feedback.
- Continuous maintenance: Plan for updates to keep application secure and responsive to user needs.

**Following factors should be consider while designing visualization application:**

- Use a consistent visual style throughout the application which will help to understand the data and to make sense of visualization.
- User clear and concise labels for the data.
- User a limited number of visual elements and visualization.

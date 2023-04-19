# Cheatsheet - Hardware - Computer Vision

## Computer Vision

### What is Computervision
Computer vision is a field of artificial intelligence and computer science that focuses on enabling computers to interpret, analyze, and understand images and videos in the same way that humans do. It involves developing algorithms and techniques that enable computers to perceive and comprehend visual information from the world around them.

Image processing, on the other hand, is a more general term that refers to the manipulation and analysis of images using computer algorithms. Image processing techniques can be used for a wide range of applications, from improving image quality to extracting features and patterns from images for further analysis.

Computer vision and image processing are related fields, but they differ in their goals and scope. While image processing focuses on manipulating and analyzing images to extract specific information, computer vision aims to replicate the complex processes of human vision, including image recognition, object detection, and scene understanding.

To achieve these goals, computer vision algorithms typically involve several steps. First, the algorithm captures an image or video stream using a camera or other input device. Then, the image is preprocessed to remove noise, adjust lighting, and enhance features. Next, the algorithm analyzes the image to identify objects, recognize patterns, and extract meaningful information. Finally, the output of the algorithm is used to make decisions, perform actions, or provide feedback to the user.

Computer vision algorithms can use a variety of techniques, including machine learning, deep learning, and neural networks. These methods allow algorithms to learn from large datasets of images and improve their accuracy over time. Additionally, computer vision algorithms can use a range of sensors, including cameras, lidar, and radar, to capture visual data in different environments and conditions.

### Computer Vision Use cases

Computer vision has a wide range of applications across many industries and fields. Here are some common applications of computer vision:

1. Object recognition and tracking: Computer vision algorithms can be used to recognize and track objects in images and videos, which is useful in fields such as security, robotics, and autonomous vehicles.

2. Facial recognition: Computer vision algorithms can analyze and recognize faces, which is used for security, law enforcement, and other applications.

3. Medical imaging: Computer vision can be used to analyze medical images, such as X-rays, CT scans, and MRIs, to detect abnormalities and diagnose diseases.

4. Augmented reality: Computer vision can be used to overlay digital information onto the real world, creating an augmented reality experience.

5. Retail and advertising: Computer vision can analyze customer behavior and preferences, and can be used to create personalized advertisements and recommendations.

6. Industrial automation: Computer vision can be used to monitor and control manufacturing processes, identify defects, and improve quality control.

7. Agriculture: Computer vision can be used to analyze crop health and growth, detect pests and diseases, and optimize harvesting.

8. Sports analysis: Computer vision can be used to analyze sports footage to track player movements, detect fouls, and analyze game strategy.

9. Education: Computer vision can be used to create interactive educational materials, such as virtual reality simulations and educational games.

10. Environmental monitoring: Computer vision can be used to monitor environmental changes, such as deforestation, sea level rise, and climate change.

### What algorithm does Computer Vision use? 

Computer vision uses a variety of algorithms, but one of the most popular and effective is convolutional neural networks (CNNs). CNNs are a type of deep learning algorithm that is inspired by the organization of the human visual system.

CNNs work by processing an image in a series of layers. Each layer consists of a set of filters that perform convolution operations on the input image. The output of each layer is then passed on to the next layer, until the final output is produced. The final output can be a classification (e.g. "this is a cat") or a segmentation (e.g. "this part of the image is a cat").

The convolution operation is performed using a filter, which is a small matrix of values. The filter is applied to a small section of the input image, and the dot product of the filter and the input is computed. This operation is repeated across the entire image, producing a new output image that has been filtered.

The filter is then moved to the next section of the input image, and the process is repeated. This produces a new filtered output image that has been convolved with the filter across the entire input image. Multiple filters can be used in a layer, producing multiple output images.

To formalize this process mathematically, let's define the input image as $I$ and the filter as $F$. The convolution operation can be expressed as:

$$ (I*F) _ {i,j} =\sum_{k,l} I_{i-k, j-l}F_{k,l}$$

Where $(I*F) _ {i,j}$ is the output of the convolution operation at location $(i,j)$, and $I_{i-k, j-l}$ and $F_{k,l}$ are the values of the input and filter at location $(i-k,j-l)$ and $(k,l)$, respectively.

This operation is performed for each location in the input image, producing a new output image that is smaller than the original input image (due to the size of the filter).

The output of each layer in a CNN is typically passed through a non-linear activation function, such as the Rectified Linear Unit (ReLU) function:

$$f(x) = \max(0, x)$$

This function introduces non-linearity into the network, which enables it to learn more complex patterns and features.

Overall, CNNs have proven to be highly effective in a wide range of computer vision tasks, including image classification, object detection, and segmentation.

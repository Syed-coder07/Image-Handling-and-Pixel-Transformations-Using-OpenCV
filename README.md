# Image-Handling-and-Pixel-Transformations-Using-OpenCV

## Developed by : Syed Shamsheer Ali B

## Register Number : 212225220114

## Aim
To write a Python program using OpenCV to read and display an image, adjust its brightness, modify its contrast, and split the image into Blue, Green, and Red channels.

## Software Required
- Anaconda – Python
- Jupyter Notebook
- OpenCV


## Algorithm

### Step 1: Read and Display an Image
Load the image `Syed1.jpg` from the local directory using OpenCV and display it.

### Step 2: Adjust Brightness
Create a matrix of ones with the `float64` data type to adjust the brightness of the original image.

### Step 3: Generate Brighter and Darker Images
Add and subtract a constant matrix from the original image to create brighter and darker versions. Display all three images.

### Step 4: Modify Image Contrast
Create two contrast-adjusted images using scaling factors of `1.1` and `1.2`, without applying an overflow correction. Display the original and modified images.

### Step 5: Split Image Channels
Split the original image into Blue, Green, and Red (BGR) components and display each channel separately.

## Program Developed By
- **Name:** : Syed Shamsheer Ali B
- **Registered Number:** 212225220114

## EXP-No-01 :  IMAGE HANDLING AND PIXEL TRANSFORMATION USING OPENCV

##  Read the image ('Syed1.jpeg') using OpenCV imread() as a grayscale image.
> ```
> import cv2
> import matplotlib.pyplot as plt
> ```

## Read the saved image above as a color image using cv2.cvtColor().
  >```
  >img = cv2.imread('Syed1.jpeg', cv2.IMREAD_COLOR)
  >```
## Original Image:
>```
>image = cv2.imread('Syed1.png') 
>img_rgb.shape
>plt.imshow(img_rgb, cmap='viridis')  
>plt.title("Original Image")
>plt.axis('off')  
>plt.show()
>```
## Convert Original Image with line from top left to right bottom
>```
>h, w = img.shape[:2]
>cv2.line(img, (0, 0), (w-1, h-1), (255, 0, 0), 3)
>plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
>plt.axis("off")
>plt.show()
>```

## Convert Original Image with Blue Circle
>```
>circle_img = cv2.circle(img_rgb.copy(), (w//2, h//2), min(w, h)//4, (0, 0, 255), 4)
>plt.imshow(circle_img)
>plt.title("Image with Blue Circle")
>plt.axis("off")
>plt.show()
>```

## Convert Original Image with Blue Rectangle border
```
height, width = img_rgb.shape[:2]
rectangle_img = cv2.rectangle(
    img_rgb.copy(),
    (0, 0),                       
    (width - 1, height - 1),      
    (0, 0, 255), 
    5
    )
>plt.imshow(rectangle_img)
>plt.title("Image with Blue Rectangle Border")
>plt.axis("off")
>plt.show()
```
## Convert Original Image with Text
>```
>import cv2
>import matplotlib.pyplot as plt
>img = cv2.imread(r"C:\Users\syedf\OneDrive\Documents\Personal\Syed1.png")
>img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
>height, width = img.shape[:2]
>plt.imshow(img_rgb)
>plt.title("Image with Text")
>plt.axis("off")
>plt.show()
>```
>
## Convert Original Image into RGB
>```
>plt.figure(figsize=(8, 6))
>plt.imshow(img_rgb)
>plt.title("Original RGB Image")
>plt.axis("off")
>plt.show()
>```
## Convert Original Image into HSV
>```
>img_hsv = cv2.cvtColor(img_rgb, cv2.COLOR_RGB2HSV)
>plt.figure(figsize=(8, 6))
>plt.imshow(img_hsv)
>plt.title("HSV Image")
>plt.axis("off")
>plt.show()
>```

## Convert Original Image into GrayScale 
>```
>gray_img = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
>plt.figure(figsize=(8, 6))
>plt.imshow(gray_img, cmap='gray')
>plt.title("Grayscale Image")
>plt.axis("off")
>plt.show()
>```

## Convert Original Image into YCrCb 
>```
>img_ycrcb = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
>plt.figure(figsize=(8, 6))
>plt.imshow(img_ycrcb)
>plt.title("YCrCb Image")
>plt.axis("off")
>plt.show()
>```

## Convert HSV Image into RGB
>```
>img_rgb = cv2.cvtColor(img_hsv, cv2.COLOR_HSV2RGB)
>plt.figure(figsize=(8, 6))
>plt.imshow(img_rgb)
>plt.title("HSV to RGB Image")
>plt.axis("off")
>plt.show()
>```

## Convert Image with Center White Block
>```
>x = (w - 600) // 2
>y = (h - 600) // 2
>cv2.rectangle(img, (x, y), (x + 600 - 1, y + 600 - 1), (255, 255, 255), thickness=-1)
>plt.figure(figsize=(8, 6))
>plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
>plt.title("Image with Center White Block")
>plt.axis("off")
>plt.show()
>cv2.imwrite("output.png", img)
>print("Image saved as output.png")
>```

## Re-Sized Image (Half)
>```
>img = cv2.imread(r"C:\Users\syedf\OneDrive\Documents\Personal\Syed1.png")
>resized = cv2.resize(img, (img.shape[1] // 2, img.shape[0] // 2))
>plt.imshow(cv2.cvtColor(resized, cv2.COLOR_BGR2RGB))
>plt.title("Image Resized (Half Size)")
>plt.axis("off")
>plt.show()
>```

## Cropped Region of Interest (ROI)
>```
>x, y = w // 2, h // 2
>roi = img[y-50:y+50, x-50:x+50]
>plt.figure(figsize=(5, 5))
>plt.imshow(roi)
>plt.title("Cropped Region of Interest (ROI)")
>plt.axis("off")
>plt.show()
>```

## Image Flipped Horizontally 
>```
>flipped = cv2.flip(img, 1)
>plt.imshow(cv2.cvtColor(flipped, cv2.COLOR_BGR2RGB))
>plt.title("Flipped Horizontally")
>plt.axis("off")
>plt.show()
>```

## Image Flipped Vertically
>```
>flipped = cv2.flip(img, 0)
>plt.imshow(cv2.cvtColor(flipped, cv2.COLOR_BGR2RGB))
>plt.title("Flipped Vertically")
>plt.axis("off")
>plt.show()
>```

## OUTPUT :

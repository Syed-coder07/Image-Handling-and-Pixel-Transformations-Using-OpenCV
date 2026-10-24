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


Original Image

<img width="367" height="500" alt="{AA3D63E9-60F4-43C5-9355-3835817BA9FB}" src="https://github.com/user-attachments/assets/5a2742a8-a6b5-460f-a5ec-897cdc1fadc2" />


line from top left to right bottom

<img width="364" height="464" alt="image" src="https://github.com/user-attachments/assets/a10170e7-ff64-49f7-9922-bf790c2b0b3a" />


Image with Blue Circle

<img width="370" height="501" alt="{1DD090DA-65F3-4304-9A3A-4E62AED4F02C}" src="https://github.com/user-attachments/assets/403eca54-d1ad-475c-9a9f-e9954ed5bd94" />


Image with Blue Rectangle border

<img width="372" height="517" alt="{0B9D8A7B-6550-47F3-BE13-57306317BD69}" src="https://github.com/user-attachments/assets/498dd3ca-a1f7-40e3-838c-01e8e44397f7" />


Image with Text

<img width="366" height="504" alt="{593537EE-6DA2-446D-B503-E79E6CD4B558}" src="https://github.com/user-attachments/assets/5bd670e9-a16a-4bb2-870b-7bda3acd5e24" />


Original Image into RGB

<img width="457" height="627" alt="{8073E9D7-8DCF-48FA-932F-77D06A791777}" src="https://github.com/user-attachments/assets/da62051d-b8ee-4ff9-8dda-d29ed063464d" />


Original Image into HSV

<img width="460" height="626" alt="{B1680742-6F6C-433C-ADD0-D5E80D072B17}" src="https://github.com/user-attachments/assets/eb06e966-f3e2-4c37-93e4-634656d36f75" />


Original Image into GrayScale 

<img width="455" height="627" alt="{F0CDDE23-BBB5-46AF-B76A-D20909F48EB1}" src="https://github.com/user-attachments/assets/5cb52a4b-4f70-4f76-a628-de7ffebf4628" />


Original Image into YCrCb 

<img width="459" height="623" alt="{A68987D7-8E28-42C3-B721-9BC1B858DB0F}" src="https://github.com/user-attachments/assets/73b6c066-6205-42e3-b7d7-52baa5bead68" />


HSV Image into RGB

<img width="457" height="622" alt="image" src="https://github.com/user-attachments/assets/4ddc739d-26ea-4fa2-a428-ec6c00d5616d" />


Image with Center White Block

<img width="460" height="616" alt="image" src="https://github.com/user-attachments/assets/a2fc0fbb-a1a1-4cc4-9dce-deb5db748820" />


Re-Sized Image (Half)

<img width="370" height="508" alt="image" src="https://github.com/user-attachments/assets/ea7e01ec-2277-4371-ba52-5e92e9661fe2" />


Cropped Region of Interest (ROI)

<img width="486" height="525" alt="image" src="https://github.com/user-attachments/assets/a53981df-e8d2-4100-8e00-ad81cb1c6685" />


Image Flipped Horizontally 

<img width="370" height="504" alt="image" src="https://github.com/user-attachments/assets/65396c13-14b4-477c-9d4e-b19faf81b996" />


Image Flipped Vertically

<img width="374" height="515" alt="image" src="https://github.com/user-attachments/assets/b8a4a5e5-e632-4a2a-b0d1-7a6817cd2de1" />

Result:

Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.

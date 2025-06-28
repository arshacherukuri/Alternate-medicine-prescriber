To execute


OCR
OCR using Tesseract and its Python wrapper library, pytesseract.
1. Install Libraries:
You can install pytesseract using the following command:
!pip install pytesseract
Additionally, you’ll need to install Tesseract itself:
!sudo apt install tesseract-ocr
2. Image Loading:
In your code, replace the placeholder image path with the actual path to the image you want to process.
Note that Colab already includes libraries like OpenCV and PIL for image loading.
3. Preprocessing:
After loading the image, perform any necessary preprocessing steps (such as resizing, denoising, or thresholding) to enhance OCR accuracy.
4. Extract Text:
Use pytesseract.image_to_string() to extract text from the image.
Provide the recognized text as input to the subsequent part of your code.
5. Get Medicine Names:
Finally, process the extracted text to obtain the medicine names you need.




ML_CODE


Certainly! Let’s break down the code and explain how to run it step by step:
1. Install Required Libraries:
   * Before running the code, ensure you have the necessary libraries installed. You’ll need:
      * pandas: For data manipulation
      * scikit-learn: For calculating Euclidean distances
      * numpy: Required by scikit-learn
      * tqdm: Optional (for progress bars during installation)
If you don’t have them installed, you can use the following commands:
!pip install pandas scikit-learn numpy tqdm
   * 2. Load the CSV Data:
   * Replace the empty string in pd.read_csv(' ') with the actual path to your CSV file containing medicine data.
   * The CSV file should have columns like ‘name’, ‘short_composition1’, and ‘short_composition2’.
3. Data Preprocessing:
   * Drop unnecessary columns (‘id’, ‘Is_discontinued’, etc.) using mydata.drop().
   * Fill any NaN values in ‘short_composition1’ and ‘short_composition2’ with spaces.
   * Merge both short compositions into a single ‘composition’ column.
   * Convert the ‘composition’ column to lowercase.
4. Recommendation Function:
   * The recommendations() function takes a medicine name and returns similar medicines.
   * It calculates Euclidean distances between the composition vectors.
   * Adjust the value of k to get more or fewer recommendations (default is 2).
5. Run the Code:
   * Replace "Avil 25 Tablet" with the medicine name you want to find alternatives for.
   * Execute the code, and it will print the top 2 similar medicines.

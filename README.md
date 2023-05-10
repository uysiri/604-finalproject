# 604-finalproject
## The Silhouettes Dataset

It's not yet possible to "try before you buy" online so most major clothing retailers include images of models in their items on their ecommerce sites to give shoppers an idea of what to expect. However, popular online second-hand markets (ie. Poshmark, Depop, EBay, Grailed, Vinted... etc.) are comprised of individuals reselling their used garments or rare specially sourced vintage or high fashion items. These individual sellers are not always able to model their listings and are not obligated to find models that can. As a result, it can be challenging for fashion-savvy consumers browsing these online markets to identify items in the styles and silhouettes that they seek. 

This dataset was designed to study 3 popular silhouettes of women's garment tops: triangle/trapeze, hourglass, and tubular-- particularly when the garment is *not* being worn on a body. The silhouette is the shape that a garment takes when worn on the body. Silhouettes are essential to personal style as different silhouettes accentuate the body in different ways. Silhouettes are created by the cut of the garment, the material used to construct the garment, and by the physique of the individual wearing the garment. Since clothing models are not always feasible for small sellers, prospective buyers would benefit from understanding the unique features of different silhouettes when they are not being worn.  

The dataset consists of 1305 35x35 images of clothing items belonging to 3 classes: 'babydoll_trapeze', 'bustier_hourglass', and 'tshirt_straight', each corresponding to a common silhouette. The 'babydoll_trapeze' class represents the triangle/trapeze silhouette. Garments that feature the triangle/trapeze silhouette have a high waist, set just under the bust and a flowing, loose bodice that flares outwards, creating a trapezoidal shape. The silhouette is created by the shape of the bodice, so the type of neckline, sleeve length, and overall length of a garment does not matter. The 'bustier_hourglass' class represents the hourglass silhouette which features a bodice with with exagerated waist indentions that accentuate the bust and the hips. If the length of the bodice extends down to the hips (ie. full length instead of cropped) then the shoulder and hip width should be nearly equal, thus creating an hourglass shape. When not worn on the body, this silhouette is ideally represented by bustier or corset tops. Since corsets and bustiers usually feature 'boning' or are made of stiff materials to cinch the waistline in an aggressive manner, they still retain an hourglass shape when not worn. The 'tshirt_straight' class represents the rectangular or tubular silhouette. As can be inferred from the name, the bodice of a tubular or rectangular garment falls in a straight line, perpendicular to the top of the shoulder and the bottom hem. This silhouette can be represented by any loose-cut t-shirt or shirt. 

 Each class contains 435 hand-selected images from the image gallery, Pinterest and bulk downloaded with *gallery-dl*. Each selection represents an unique garment from the target class either lying flat or on a hanger. The majority of the selected images were not professionally taken and were posted on Pinterest by resellers/sellers to represent their item listings on resale markets. Selecting these types of images preserves some of the variance in angles, exposures, and photo perspectives that an actual consumer would encounter when browsing listings from different sellers. The downloaded images were additionally preprocessed with *rembg* to remove noise contributed by backgrounds and *tensorflow* to remove color channels from the images, create class labels from subdirectory folder names, as well as uniformly resize all images to 35x35 pixels. The decision to remove backgrounds from the images stemmed from the reality that many of the images were not professionally taken. Images of garments were taken on top of brightly patterned bedding, grass, carpets, etc. that could create unwanted distractions from the focal point of the image. At the same time, removing backgrounds does not change the variations in lighting, angles, and photo perspectives of the actual items in the images. The images were transformed to grayscale because a garment's color or pattern does not define it's silhouette.

## to Replicate
To run this project, clone this repository which includes the target datasets "images.npy" and "labels.npy"
- This project is a jupyter notebook which requires anaconda3/ipykernel/jupyternb
- Install the following dependencies: numpy, matplotlib, pandas, scikit-learn, seaborn
- Open "604finalproject.ipynb" and run from the top --> if replicating, I highly advise against re-running the GridsearchCV instances because it can take hours. Instead, the outcomes have already been saved as .csv files named throughout the code. You can read them back into the notebook for analysis with pd.read_csv("name_of_file.csv")



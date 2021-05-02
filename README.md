# IG_Image_scraper

Scrape images from Instagram public profiles through python and selenium. Download chrome driver from following link. Please make sure that chrome browser in the system is compatible with chrome driver - https://chromedriver.chromium.org/downloads 

ImageScraper_Instagram_FullScreen.ipynb opens Instagram in full screen mode, opens the profile or hashtag mentioned in the file. From the profile, 'src' of all 'img' tags are scrapped and saved to text files. Further, the text files are read, find all unique links and downloads the images. FYI - If the tile has multiple photos, only the first photo is taken for consideration and downloaded. 

ImageScraper_Instagram_MobileView.ipynb opens Instagram in mobile mode, opens the profile or hashtag mentioned in the file. From the profile, 'src' of all 'img' tags are scrapped and saved to text files. Further, the text files are read, find all unique links and downloads the images. FYI - All the photos in the tile will be downloaded in mobile view. 

Most possible exceptions are handelled through Try - Except blocks. 

Requirements: 
pip install selenium 
pip install wget 
pip install tqdm



--------------- Inputs are to be given in the first cell of notebook -------------------------------

### Instagram Username and Password
IG_username = "Enter username here" ### -- ENTER USERNAME HERE
IG_password = "Enter password here" ### -- ENTER PASSWORD HERE

chromedriver_path = "chromedriver.exe" ## CHANGE CHROME DRIVER PATH HERE

### Give profile name of user as string ###Give Hashtags with '#' before the string
profiles_hashtags = [
    #Profiles Below
    "instagram",
    "creators"
    
    #Hashtags here
    "#pencil",
    "#Sketch"
    ]
textfile_name = "instagram_pics" ## Enter text file name, that saves all image URLs. [Multiple files are created]
folder_name = "IG_Pictures" ## Folder Name to save all images - Creates a folder if not available.


import os

downloadsFolder = "/Users/ycedeno/Downloads/"

imageFolder = "/Users/ycedeno/Documents/Organizer/Images/"
AudioFolder = "/Users/ycedeno/Documents/Organizer/Audios/"
VideoFolder = "/Users/ycedeno/Documents/Organizer/Videos/"
pdfFolder = "/Users/ycedeno/Documents/Organizer/PDF/"
xlsFolder = "/Users/ycedeno/Documents/Organizer/Files/"


if __name__ == "__main__":
    for filename in os.listdir(downloadsFolder):
        name, extension = os.path.splitext(downloadsFolder + filename)

        if extension in [".jpg", ".jpeg", ".png"]:
            os.rename(downloadsFolder + filename, imageFolder + filename)

        if extension in [".mp4"]:
            os.rename(downloadsFolder + filename, VideoFolder + filename)

        if extension in [".mp3"]:
            os.rename(downloadsFolder + filename, AudioFolder + filename)

        if extension in [".xls",".xlsx",".csv"]:
            os.rename(downloadsFolder + filename, xlsFolder + filename)

        if extension in [".pdf"]:
            os.rename(downloadsFolder + filename, pdfFolder + filename)

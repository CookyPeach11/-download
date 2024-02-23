# -download
import requests

class Downloader:
    def __init__(self):
        pass

    def download_file(self, url, filename):
        response = requests.get(url)
        with open(filename, 'wb') as f:
            f.write(response.content)
        print(f"File downloaded successfully: {filename}")

# Example usage
downloader = Downloader()
downloader.download_file("https://example.com/file.zip", "file.zip")
downloader.download_file("ftp://ftp.example.com/file.txt", "file.txt")

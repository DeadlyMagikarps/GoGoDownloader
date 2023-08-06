
<div align="center">
  <img
    style="width: 300px; height: 300px"
    src="https://github.com/karl0ss/GoGoDownloader/raw/master/img/gogo_logo.png"
    title="GoGoDownloader"
    alt="GoGoDownloader"
  />
  <h3>GoGo Downloader</h3>
  <h4>Forked from <a href="https://github.com/sh1nobuu/BitAnime">BitAnime</a></h4>
  <p>
    A Python script that allows you to download all of an anime's episodes at once.
  </p>
 
</div>

## About GoGo Downloader

GoGo Downloader is based on the now broken **BitAnime**. I have had to rework quite a bit of the code to get it working again, and have ideas for some other improvements, I don't want to mess with the original codebase too much, hence **GoGo Downloader**.

**GoGo Downloader** gets its content from [gogoanime](http://gogoanime3.net). If you get a **404** error, please look up the correct anime name on [gogoanime](http://gogoanime3.net). The application will let you download all the episodes, or you can choose how many episodes you want to download.

GoGo Anime has changed the way they show download links, and this no longer works via BS4, as the recaptcha blocks the links, but if you are logged in, there are other routes to get to download links, I have taken one of these routes to restore the application.

## Features

- Download all qualities options from GoGoAnime
- Update the current GoGoAnime domain via config file (as they keep changing it)
- Specify the number of concurrent downloads via config file (Max is 6)
- Set file overwrite via config file (0 = Skip / 1 = Overwrite)

## Installation
You have 2 options here, you can download the exe on the releases page and run on Windows

- Download the zip
- Extract and set your GoGoAnime Username and Password in the config.json
- Run the exe

If you want to run from source, or are using Linux/Mac you can run directly from source doing the following - 

- `git clone https://github.com/karl0ss/GoGoDownloader.git`
- `pip install -r requirements.txt`
- Create config.json from config.json.default
- Add your GoGoAnime Username and Password to config.json (Can't be a Google account)
- Run the app with `python GoGoDownloader.py`

## Screenshot

<div align="center">
  <img style="height:386px; width:688px;" src="https://github.com/karl0ss/GoGoDownloader/raw/master/img/screenshot.png"
  title="BitAnime in action" alt="BitAnime Screenshot">
</div>

## Dependencies

**GoGo Downloader** is highly reliant on the python modules `requests`, `colorama`, `parfive`, and `BeautifulSoup`.

## Usage

The anime name is separated by "-". You can either type it manually, or go to [gogoanime.gg](https://gogoanime3.gg/) and search for the anime you want to download and copy the name from the URL.

### Examples

##### One word title

- https://gogoanime3.gg/category/bakemonogatari >> bakemonogatari
- https://gogoanime3.gg/category/steinsgate >> steinsgate

##### Multiple word title

- https://gogoanime3.gg/category/shadows-house >> shadows-house
- https://gogoanime3.gg/category/kono-subarashii-sekai-ni-shukufuku-wo- >> kono-subarashii-sekai-ni-shukufuku-wo-


# GoGoDownloader CLI
I have now also created the GoGoDownloader CLI, this tool can be used to run on a scheduled basis, it will login and get the latest episodes from your GoGoAnime bookmarks, and download the latest episode if it has not been downloaded yet.
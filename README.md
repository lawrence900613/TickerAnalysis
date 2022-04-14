# TickerAnalysis

This software attempts to provide a buy/sell recommendation of a particular stock ticker based on technical indicators and news article analysis.

# Setup

Ensure the following packages are installed. Versions shown are the minimum versions that have confirmed to be working in an Windows environment.

Pandas 1.4.1

NumPy 1.22.3

Requests 2.27.1

nltk 3.7

To query the IEXCloud API for data, an IEXCloud account and their API tokens are also required. Rename config_template.cfg and copy-paste the keys into their corresponding fields to enable this functionality.

# Usage

Unpack files into any directory you wish. It will be referred here forth as "the directory".

## Fetching Data

  In the directory, use command `python .\Fetch.py` to fetch data required from IEX Cloud. Follow the prompts as shown.
  
  If the API returns a valid object, the program will exit without any output, and a new file "data.json" is saved in the directory.
  
  Otherwise, the program will raise an exception and the error is outputted to the console.
  
## Analysing the Data

  In the directory, use command `python .\analysis.py` to analyse the stock desired. Follow the prompts as shown.
  
  If the corresponding data does not exist in data.json, the console will ask you to fetch the data required first, and exits.
  
  If the program ran successfully, the resulting scores from each indicator, as well as the aggregated score, will be outputted to the console, with their corresponding recommended course of action. A graph will also be produced, showing the historical price, RSI and stochastic oscillator levels. No new files are produced.

# Legalese

### Disclaimer

No part of information provided through the software or this GitHub page is financial advice, and should not be construed as such.

The authors bear no responsibility of any profit generated or loss incurred by the user based on the information generated by the software.

### Copyright & Licence

Copyright 2022 Eric Chen, Shao-en Hung Lawrence and Jun Pin Foo.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

# Footnote
This project will also act as the final project of Spring 2022 CMPT353 D100 at SFU for Eric Chen, Shao-en Hung Lawrence and Jun Pin Foo. 

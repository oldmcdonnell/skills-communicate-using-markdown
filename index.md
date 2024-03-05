# Markdown Lesson
###### This is an index file for markdown in Github 
<h1> H1 works the same as #</h1>
<h6>H6 works the same as 6 x # </h6>

##Images…
<img alt="painting" src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/e6bdf89f-5875-4ac1-9b1a-50eee90c58a7/d2f3h3k-3f7690b5-efbb-46ed-bfbe-f3de58082790.jpg/v1/fit/w_828,h_1274,q_70,strp/some_arts_a1_by_aliramojo_d2f3h3k-414w-2x.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTI4NiIsInBhdGgiOiJcL2ZcL2U2YmRmODlmLTU4NzUtNGFjMS05YjFhLTUwZWVlOTBjNThhN1wvZDJmM2gzay0zZjc2OTBiNS1lZmJiLTQ2ZWQtYmZiZS1mM2RlNTgwODI3OTAuanBnIiwid2lkdGgiOiI8PTgzNiJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.KOayXeS4gZHi4irQu8_cDmu7_PSFtBSPyLLCTlss_9U">

##code
``` python
from flask import Flask, render_template
import pandas as pd


app = Flask(__name__)
df = pd.read_csv("data/dictionary.csv")

@app.route('/')
def home():
    return render_template("home.html")


@app.route('/api/v1/<word>/')
def api(word):
    definition = df.loc[df["word"] == word]['definition'].squeeze()
    result_dictionary = {'word': word, 'definition': definition}
    return result_dictionary


if __name__ == "__main__":
    app.run(debug=True, port=5001)
```
---
- [x] Create resposiotry
- [x] Pull request
- [x] Edit index.md
- [ ] Finish Markdown lesson
- [ ] Add files to assignment
- [ ] Continute with the rest of the assignments 

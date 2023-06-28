
### Workflow to turn Jupyter notebook into presentation slides

- fork the reveal.js github sources to your new github repo
- go to repo settings and make Github pages point to master branch
- see that pages build fine: reveal.js's test presentation should be visible at your Github pages
- Make a Jupyter notebook that should be turned into presentation
- Click on Settings ("wheels" on right-hand border) and then "Common tools"
- Each cell should be tagged as "Slide" for new slide or "Fragment" for incremental slide build
- Save and export notebook as reveal.js slides
- Copy resulting slides.slides.html into index.html of your local repo
- You should install repo as per reveal.js instructions. 
- Than `npm start` will start a web server on localhost where your slides will be visible. (This step failed in my
   case. I needed to clone directly reveal.js repo and install that.)
- When you are happy push new index.html to your Github repo and corresponding Github pages should be build automatically
- You can avoid Github and Github pages altogether by installing `decktape` and converting your slides to PDF by `decktape http://localhost:8000 slides.pdf`

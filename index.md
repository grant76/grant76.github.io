## Sound Sleep


### Project Idea

Studying sound's impact on sleep quality.


### Proposal

Implementing a machine learning algorithm to determine optimal ambient noise levels to improve sleep.


### Inputs and Tests

- Environmental Input

  - Volume and type of sounds
  
- Machine Learning Input 
  - Magnitude and frequency of ambient noise
  - Movement of participant before and during sleep 
  - Time required to fall asleep
  - Sleep quality


### Methods and Observations

- Subject individuals to different types of sounds and at different volumes. Research sleep quality papers.  
- Track individual’s movement through IMU sensors on Arduino Nano 33 BLE Sense.  
- Measure noise levels of the sleeping environment using Arduino’s microphone.  
- Use a neural network on Arduino to predict ideal noise levels.  
- Train the neural network with data collected from the Arduino’s sensors.


### Outputs and Metrics

- Sensor Output
  - Time taken to fall asleep 
  - Frequency and magnitude of movement
  
- User Output
  - Quality of sleep
  
- ML Output
  - Noise level that maximizes quality of sleep


## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/grant76/grant76.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/grant76/grant76.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

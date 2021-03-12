# Carbon Bot

Carbon Bot lets you calculate the emissions from air travel, and suggests UN-certified projects you can donate to.
These projects can issue Certified Emissions Reductions, read more [here](https://offset.climateneutralnow.org/allprojects)

To talk to Carbon Bot, go to https://m.me/CarbonBot.from.Rasa

See carbon bot [in the news!](https://www.zdnet.com/article/feel-guilty-about-flying-heres-a-robot-thatll-make-you-feel-better/)

This is a research project from [Rasa](https://rasa.com/research) and it is built with [Rasa Open Source](https://github.com/RasaHQ/rasa) and [Rasa X](https://rasa.com/docs/rasa-x/)


# Updating the used Rasa Open Source / Rasa X Versions

To update the used Rasa / Rasa X versions please check the following files:
- `.env`
- `requirements.txt`

**Be Warned** There is a lot of NSFW content in the training data!

# Howto run
Install dependencies
```bash
pip install rasa==1.10.22
pip install tensorflow_text==2.1.1
```

Some models were removed and config needs to be changed
```yaml
- name: ConveRTTokenizer
  model_url: https://github.com/connorbrinton/polyai-models/releases/download/v1.0/model.tar.gz
- name: ConveRTFeaturizer
  model_url: https://github.com/connorbrinton/polyai-models/releases/download/v1.0/model.tar.gz
```

# Useful commands
Run the rasa server: `rasa run --enable-api --endpoints endpoints.yml`
Run action server: `rasa run actions`
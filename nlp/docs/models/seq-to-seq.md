# Seq-to-Seq Models and Applications

Seq-to-Seq models in NLP are designed to process an input sequence and generate an output sequence, making them ideal for tasks that require understanding and transformation of text. They are widely used in translation, summarization, and question-answering.

Go [here](https://github.com/ilsilfverskiold/transformers-nlp-docs/blob/main/docs/business-cases/seq-to-seq.md) to get examples for different **business cases** for seq-to-seq models. 

## Pre-training Objective
- **Feature Extraction**
  
## Base Models

### T5 (Text-To-Text Transfer Transformer)
- **Overview**: A versatile model that converts all NLP tasks into a text-to-text format.
- **Released**: October 2019
- **Developed by**: Google Research.
- **Models in Hugging Face**:
  - [T5-small (60.5M)](https://huggingface.co/t5-small)
  - [T5-base (223M)](https://huggingface.co/t5-base)

### BART (Bidirectional and Auto-Regressive Transformers)
- **Overview**: Combines bidirectional context encoding and autoregressive decoding, useful for both understanding and generation tasks.
- **Released**: October 2019
- **Developed by**: Facebook AI.
- **Models in Hugging Face**:
  - [BART-base (139M)](https://huggingface.co/facebook/bart-base)
  - [BART-large](https://huggingface.co/facebook/bart-large)
 
## Tasks to Train For

### Machine Translation
- **Examples**: Translating text from one language to another.
  - [translation-en-pt-t5](https://huggingface.co/unicamp-dl/translation-en-pt-t5?text=My+name+is+Wolfgang+and+I+live+in+Berlin)
 
### Text Generation
- **Examples**: Generating text.
  - [t5-base-keywords-to-headline](https://huggingface.co/EnglishVoice/t5-base-keywords-to-headline?text=headline%3A+weight+loss)

### Text Summarization
- **Example**: Condensing long text into shorter summaries.
  - [BART-large-cnn (406M)](https://huggingface.co/facebook/bart-large-cnn)
  - [BART-summarization](https://huggingface.co/slauw87/bart_summarisation)
  - [bart-paraphrase](https://huggingface.co/eugenesiow/bart-paraphrase?text=They+were+there+to+enjoy+us+and+they+were+there+to+pray+for+us.)

### Keyword Extraction (Text Summarization/Text Generation)
- **Example**: Generating keywords to summarize text.
  - [h2-keywordextractor](https://huggingface.co/transformer3/H2-keywordextractor)
  - [tech-keywords-extractor](https://huggingface.co/ilsilfverskiold/tech-keywords-extractor?text=AWS+Config+Rule+w.+Remediation+Set+to+SNS+Notification+-+How+to+find+which+parameters+are+exposed+to+the+message%3F)

### Question Answering
- **Example**: Generating answers to questions based on given text.
  - [bart-large-finetuned-squadv1](https://huggingface.co/valhalla/bart-large-finetuned-squadv1)
  - [finetuned-bart-for-conversation-summary](https://huggingface.co/kabita-choudhary/finetuned-bart-for-conversation-summary?text=Laurie%3A+So%2C+what+are+your+plans+for+this+weekend%3F%0AChristie%3A+I+don%E2%80%99t+know.+Do+you+want+to+get+together+or+something%3F%0ASarah%3A+How+about+going+to+see+a+movie%3F+Cinemax+26+on+Carson+Boulevard+is+showing+Enchanted.+Laurie%3A+That+sounds+like+a+good+idea.+Maybe+we+should+go+out+to+eat+beforehand.%0ASarah%3A+It+is+fine+with+me.+Where+do+you+want+to+meet%3F%0AChristie%3A+Let%E2%80%99s+meet+at+Summer+Pizza+House.+I+have+not+gone+there+for+a+long+time.%0ALaurie%3A+Good+idea+again.+I+heard+they+just+came+up+with+a+new+pizza.+It+should+be+good+because+Summer+Pizza+House+always+has+the+best+pizza+in+town.%0ASarah%3A+When+should+we+meet%3F%0AChristie%3A+Well%2C+the+movie+is+shown+at+2%3A00PM%2C+4%3A00PM%2C+6%3A00PM+and+8%3A00PM.%0ALaurie%3A+Why+don%E2%80%99t+we+go+to+the+2%3A00PM+show%3F+We+can+meet+at+Summer+Pizza+House+at+noon.+That+will+give+us+plenty+of+time+to+enjoy+our+pizza.%0ASarah%3A+My+cousin+Karen+is+in+town.+Can+I+bring+her+along%3F+I+hate+to+leave+her+home+alone.%0AChristie%3A+Karen+is+in+town%3F+Yes%2C+bring+her+along.+Laurie%2C+you+remember+Karen%3F+We+met+her+at+Sara%E2%80%99s+high+school+graduation+party+two+years+ago.%0ALaurie%3A+I+do+not+quite+remember+her.+What+does+she+look+like%3F%0ASarah%3A+She+has+blond+hair%2C+she+is+kind+of+slender%2C+and+she+is+about+your+height.%0ALaurie%3A+She+wears+eyeglasses%2C+right%3F%0ASarah%3A+Yes%2C+and+she+was+playing+the+piano+off+and+on+during+the+party.%0ALaurie%3A+I+remember+her+now.+Yes%2C+do+bring+her+along+Sara.+She+is+such+a+nice+person%2C+and+funny+too.%0ASarah%3A+She+will+be+happy+to+meet+both+of+you+again.%0AChristie%3A+What+is+she+doing+these+days%3F%0ASarah%3A+She+graduated+last+June%2C+and+she+will+start+her+teaching+career+next+week+when+the+new+school+term+begins.%0ALaurie%3A+What+grade+is+she+going+to+teach%3F%0ASarah%3A+She+will+teach+kindergarten.+She+loves+working+with+kids%2C+and+she+always+has+such+a+good+rapport+with+them%0AChristie%3A+Kindergarten%3F+She+must+be+a+very+patient+person.+I+always+think+kindergarten+is+the+most+difficult+class+to+teach.+Most+of+the+kids+have+never+been+to+school%2C+and+they+have+e+never+been+away+from+mommy+for+long.%0ASarah%3A++I+think+Karen+will+do+fine.+She+knows+how+to+handle+young+children%0ALaurie%3A+I+think+the+first+few+weeks+will+be+tough.+However%2C+once+the+routine+is+set%2C+it+should+not+be+too+difficult+to+teach+kindergarten.%0AChristie%3A+You+are+right.+The+kids+might+even+look+forward+to+going+to+school+since+they+have+so+many+friends+to+play+with.%0ASarah%3A+There+are+so+many+new+things+for+them+to+do+at+school+too.+They+do+a+lot+of+crafts+in+kindergarten.+I+am+always+amazed+by+the+things+kindergarten+teachers+do.+%0ALaurie%3A+Yes%2C+I+have+seen+my+niece+come+home+with+so+many+neat+stuff.%0AChristie%3A+Maybe+we+can+ask+Karen+to+show+us+some+of+the+things+that+we+can+do+for+this+Halloween.%0ALaurie%3A+Maybe+we+can+stop+by+the+craft+store+after+the+movie.+What+do+you+think%2C+Sara%3F%0ASarah%3A+I+will+talk+to+her.+I+think+she+will+like+that.+It+will+help+her+with+school+projects+when+Halloween+comes.%0AChristie%3A+Michael%E2%80%99s+is+a+good+store+for+crafts.+It+always+carries+a+variety+of+things%2C+and+you+can+find+almost+anything+there.%0ALaurie%3A+There+is+a+Michaels+store+not+far+away+from+Cinemax+26.+I+believe+it+is+just+around+the+corner%2C+on+Pioneer+Avenue.+We+can+even+walk+over+there.%0ASarah%3A+So%2C+we+plan+to+meet+for+pizza+at+noon%2C+go+to+the+movies+at+two%2C+and+shop+at+Michael%E2%80%99s+afterward.+Right%3F%0ALaurie+and+Christie%3A+Yes.)

The list is not exhaustive. Please visit [Hugging Face Model Hub](https://huggingface.co/models) for more.

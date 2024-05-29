## Deploying an ml model 
- can use gradio

first train the ml model
install and import pickle library

``` python

import pickle 

from sklearn.ensemble import RandomForestClassifier
clf = RandomForestClassifier(random_state=42)
clf.fit(X_train, y_train) 

# If you've fitted the model just type this to save it: Remember to change the file name
with open("filename.pkl", "wb") as f:
pickle.dump(clf, f)  

# to load the pickle file

with open("filename.pkl", "rb") as f:
	clf  = pickle.load(f)


import gradio

def make_prediction(age, employment_status, bank_name, account_balance):
    with open("filename.pkl", "rb") as f:
        clf  = pickle.load(f)
        preds = clf.predict([[age, employment_status, bank_name, account_balance]])
    if preds == 1:
            return "You are eligible for the loan"
    return "You are not eligible for the loan"

#Create the input component for Gradio since we are expecting 4 inputs

age_input = gr.Number(label = "Enter the Age of the Individual")
employment_input = gr.Number(label= "Enter Employement Status {1:For Employed, 2: For Unemployed}")
bank_input = gr.Textbox(label = "Enter Bank Name")
account_input = gr.Number(label = "Enter your account Balance:")
# We create the output
output = gr.Textbox()


app = gr.Interface(fn = make_prediction, inputs=[age_input, employment_input, bank_input, account_input], outputs=output)
app.launch()

```

So let’s unwrap what we have above:

We'll start at the point where we created the input component. You can choose to create the component in the gr.Interface, but in the following code, I built it directly outside of the gr.Interface and then provided the variable into the gr.Interface.

So, if you want to make a component that receives numbers, use gr.Number, and then from the output variable I created, you can pass text as we did earlier in our first app (the " text" string is shorthand for textbox if you don't want to declare the attribute explicitly).

Also I used the label parameter in each component so that the user will know what to do. We are already familiar with the other code mentioned above.  And now that we've done that our model is deployed.

----



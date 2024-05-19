# gemini-chat-demo
Creating Chat Demo using Google Gemini using Python and Google Colab

**Follow the code**


**import package**  <br>
import google.generativeai as genai

**Configure the Key**  <br>
you have to generate a KEY to use Google Gemini model <br><br>
googleKey="<ENTER_KEY>"  <br>
genai.configure(api_key=googleKey) <br><br>

**Select model** <br>
Based on the use case we need to select model, here we are dealing with text so we use the gemini-pro <br>
If we deal with image and video then we need to use the gemini-pro-vision model <br><br>
model = genai.GenerativeModel('gemini-pro')

**Asking question** <br><br>
chat=model.start_chat(history=[])  <br><br>

while True: <br>
  question=input("Enter Question:")   <br>
  if(question == "Done"): <br>
    break <br>
  else:  <br>
    response = chat.send_message(question) <br>
    print(response.text) <br>

  

# Game_pass
import easygui
easygui.msgbox('Before you play this game.You should tell us your Identity message!')
#name
while True:
  real_name = easygui.enterbox('Tell us your real name:')
  real_name_01 = easygui.enterbox('Write again:')
  if real_name == real_name_01:
    break
  elif real_name != real_name_01:
    easygui.msgbox('Please tell us your correct real name!')
#old
while True:
  old = easygui.enterbox('How old are you?')
  class Old():
    def __init__(self):
      self.sentence_one = 'You are on age. You can play this game whatever you want! But you have to tell us your country.'
      self.sentence_two = 'Seens you are not on age. You cannot play this game...'
  old_01 = Old()
  if int(old) >= 18:
    easygui.msgbox(old_01.sentence_one)
    break
  elif int(old) < 18:
    easygui.msgbox(old_01.sentence_two)
#country
while True:
  country = easygui.enterbox('Where are you from?')
  class Country():
    def __init__(self):
      self.sentence_three = 'Your country allow you to play this game.Now you can create an account!'
      self.sentence_four = "Seens your country doesn't allow you to play this game..."
  country_01 = Country()
  if country == 'America' or country == 'England' or country == 'Japan' or country == 'Russia':
    easygui.msgbox(country_01.sentence_three)
    break
  elif country != 'America' or country != 'England' or country != 'Japan' or country != 'Russia':
    easygui.msgbox(country_01.sentence_four)
#register and login account
easygui.msgbox('Now you have to register an account to play this game.')
userName = easygui.enterbox('Your username:')
userPwd = easygui.enterbox('Your password:')
class Account():
  def __init__(self):
    self.one = 'Login successful'
    self.two = 'Login unsuccessful'
account = Account()
easygui.msgbox('You register an account successfully! Now login your account.')
while True:
  userName_01 = easygui.enterbox('Login your username:')
  user_Pwd_01 = easygui.enterbox('Login your password:')
  if userName_01 == userName and user_Pwd_01 == userPwd:
    easygui.msgbox(account.one + '.You can play this game!')
    break
  else:
    easygui.msgbox(account.two + '.Please try again.')

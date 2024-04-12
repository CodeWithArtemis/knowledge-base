
### Install and Import

```bash
$ pip install streamlit
```

```python
import streamlit as st
```

### Add Widgets to Sidebar

```python
a = st.sidebar.radio('Choose:', [1, 2])
```

### Magic Commands

```python
'_This_ is some __Markdown__'
a = 3
'dataframe:', data
```

### Command Line

```bash
$ streamlit --help
$ streamlit run your_script.py
$ streamlit hello
$ streamlit config show
$ streamlit cache clear
$ streamlit docs
$ streamlit --version
```

### Pre-release Features

```bash
pip uninstall streamlit
pip install streamlit-nightly --upgrade
```

### Display Text

```python
st.text('Fixed width text')
st.markdown('_Markdown_')
st.caption('Balloons. Hundreds of them...')
st.latex(r''' e^{i\pi} + 1 = 0 ''')
st.write('Most objects')  # df, err, func, keras!
st.write(['st', 'is <', 3])  # see *
st.title('My title')
st.header('My header')
st.subheader('My sub')
st.code('for i in range(8): foo()')
```

### Display Data

```python
st.dataframe(my_dataframe)
st.table(data.iloc[0:10])
st.json({'foo': 'bar', 'fu': 'ba'})
st.metric(label="Temp", value="273 K", delta="1.2 K")
```

### Display Media

```python
st.image('./header.png')
st.audio(data)
st.video(data)
```

### Columns

```python
col1, col2 = st.columns(2)
col1.write('Column 1')
col2.write('Column 2')
```

### Tabs

```python
tab1, tab2 = st.tabs(["Tab 1", "Tab2"])
tab1.write("this is tab 1")
tab2.write("this is tab 2")
```

### Control Flow

```python
st.stop()
st.experimental_rerun()
```

### Personalize Apps for Users

```python
if st.user.email == 'jane@email.com':
    display_jane_content()
elif st.user.email == 'adam@foocorp.io':
    display_adam_content()
else:
    st.write("Please contact us to get access!")
```

### Display Interactive Widgets

```python
st.button('Hit me')
st.data_editor('Edit data', data)
st.checkbox('Check me out')
st.radio('Pick one:', ['nose', 'ear'])
st.selectbox('Select', [1, 2, 3])
st.multiselect('Multiselect', [1, 2, 3])
st.slider('Slide me', min_value=0, max_value=10)
st.select_slider('Slide to select', options=[1, '2'])
st.text_input('Enter some text')
st.number_input('Enter a number')
st.text_area('Area for textual entry')
st.date_input('Date input')
st.time_input('Time entry')
st.file_uploader('File uploader')
st.download_button('On the dl', data)
st.camera_input("一二三,茄子!")
st.color_picker('Pick a color')
```


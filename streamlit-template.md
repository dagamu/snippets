```python
import streamlit as st


st.title('My Streamlit App')
st.write('Welcome to my Streamlit app!')

# SECTION I
st.markdown('## Section 1: Introduction')
st.write('This is an introduction to my Streamlit app.')

# SECTION II
st.markdown('## Section 2: Data Visualization')
st.write('Here, you can visualize your data using various plots and charts.')

# SIDEBAR
st.sidebar.markdown('## Sidebar')
option = st.sidebar.selectbox(
    'Select an option',
    ('Option 1', 'Option 2', 'Option 3')
)

# CONDITIONAL CONTENT
if option == 'Option 1':
    st.write('You selected Option 1.')
elif option == 'Option 2':
    st.write('You selected Option 2.')
else:
    st.write('You selected Option 3.')

# UPLOAD FILE
uploaded_file = st.file_uploader("Upload a file")
if uploaded_file is not None:
    # Perform data processing here
    st.write('File uploaded successfully!')
    st.write('Displaying data...')

# FOOTER
st.markdown('---')
st.write('Footer: This is a Streamlit app.')

# Run the app
if __name__ == '__main__':
    st.run()
```
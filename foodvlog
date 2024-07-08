import streamlit as st
import pandas as pd

# Sample data for Maharashtrian, South Indian, and North Indian dishes
data = {
    'Category': ['Maharashtrian', 'Maharashtrian', 'South Indian', 'South Indian', 'North Indian', 'North Indian'],
    'Dish': ['Pav Bhaji', 'Misal Pav', 'Dosa', 'Idli', 'Butter Chicken', 'Paneer Tikka'],
    'Description': ['Spicy vegetable mash served with bread', 'Spicy sprouted lentils with bread', 'Fermented rice pancake', 'Steamed rice cake', 'Chicken cooked in buttery tomato sauce', 'Marinated cottage cheese grilled in tandoor'],
    'Image': ['pav_bhaji.jpg', 'misal_pav.jpg', 'dosa.jpg', 'idli.jpg', 'butter_chicken.jpg', 'paneer_tikka.jpg']
}

df = pd.DataFrame(data)

def main():
    st.title('Food Vlogging App')
    st.header('Explore Maharashtrian, South Indian, and North Indian Menus')

    category = st.selectbox('Select a Cuisine', ['Maharashtrian', 'South Indian', 'North Indian'])

    filtered_df = df[df['Category'] == category]

    st.subheader(f'{category} Dishes:')
    for index, row in filtered_df.iterrows():
        st.write(f"**{row['Dish']}**")
        st.image(f"images/{row['Image']}", caption=row['Description'], use_column_width=True)
        st.write('---')

    st.write('---')
    st.write('Developed by Your Name')

if __name__ == '__main__':
    main()

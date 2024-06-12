# Enhancing Baseball Strategy: Classifying Pitch Outcomes on Taken Pitches

## Table of Contents

- [Project Description](#project-description)
- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Dependencies](#dependencies)
- [Contributors](#contributors)
- [Acknowledgements](#acknowledgements)
- [License](#license)

## Project Description

The goal of this project is to develop a classification model that will predict whether a pitch will be called a strike (1) or a ball (0) when the batter does not swing at it. Predicting whether a taken pitch will be called a strike is a key project for baseball teams. This model allows teams to leverage predictions of strike or ball calls for various applications, such as evaluating catcher framing, making swing decisions, and analyzing umpire tendencies.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/caleb10miller/Classifying-Pitch-Outcomes.git
    ```
2. Navigate to the project directory:
    ```sh
    cd Classifying-Pitch-Outcomes
    ```
3. Install the required dependencies:
    ```sh
    pip install -r requirements.txt
    ```

## Usage

1. Prepare the dataset:
    - Ensure the dataset is properly stored in your directory.
2. Open the Jupyter Notebook:
    ```sh
    jupyter notebook G15-Project.ipynb
    ```
3. Follow the steps in the notebook:
    - Data preprocessing
    - Exploratory data analysis (EDA)
    - Training the models
    - Evaluating the models

## Data

The dataset that we acquired is a collection of pitches from the 2022 MLB Season where the batter did not swing at the pitch. This dataset was sourced from [Baseball Savant](https://baseballsavant.mlb.com/) and has 351,062 rows and 20 columns. 

### Column Breakdown

- game_pk : unique identifier for a specific game - data type is an integer
- game_date : the date on which the game occurred in the format MM/DD/YYYY - data type is date
- at_bat_number : unique identifier for a specific plate apperance - data type is an integer
- pitch_number : pitch number within the plate appearance - data type is integer
- pitch_type : identifies what type of pitch was thrown - data type is string
    - can be one of:
        - CH : changeup
        - CS, CU : curveball
        - EP : eephus
        - FA, FF : four seam fastball
        - FC : cutter
        - FS : splitter
        - KC : knuckle curve
        - KN : knuckleball
        - SI : sinker
        - SL : slider
- pitcher_name : name of the pitcher in lastname, firstname format - data type is string
- pitcher : unique identifier for pitcher - data type is integer
- batter : unique identifier for batter - date type is integer
- catcher : unique identifier for catcher - data type is integer
- description : describes whether a pitch was called a ball or strike - data type is string
- zone : describes the zone location a ball when it crosses the plate - data type is integer
- stand : whether the batter is left-handed or right-handed - data type is string
    - can be one of:
        - L : left-handed
        - R : right-handed
- p_throws : whether the pitcher is left-handed or right-handed - data type is string
    - can be one of:
        - L : left-handed
        - R : right-handed
- balls : how many balls are in the count at the time of the pitch - data type is integer
- strikes : how many strikes are in the count at the time of the pitch - data type is integer
- plate_x : horizontal position of the ball when it crosses the plate - data type is float
    - center of the plate is 0,0, units in feet 
- plate_z : vertical position of the ball when it crosses the plate - data type is float
    - the ground is 0,0, units in feet 
- sz_top : top of the batter's strike zone - set by the operator when the ball is halfway to the plate - data type is float
- sz_bottom : bottom of the batter's strike zone - set by the operator when the ball is halfway to the plate - data type is float
- broadcast : Link to a video of the pitch - data type is string

## Dependencies

python: 3.11.2\
pandas: 2.2.1\
numpy: 1.26.4\
matplotlib: 3.8.3\
scipy: 1.12.0\
seaborn: 0.13.2\
imblearn: 0.12.2\
scikit-learn: 1.4.2\
xgboost: 2.0.3\
tensorflow: 2.16.1\
scikeras: 0.13.0

## Contributors

- Caleb Miller - caleb10miller@gmail.com - [Personal Site](https://www.calebzmiller.com)
- Robert Logovinsky - robert.logovinsky@gmail.com
- Hashim Afzal - hashimafzal@hotmail.com

## Acknowledgements

This data was provided by the Philadelphia Phillies for a hackathon event. We are grateful for the opportunity to work with this comprehensive dataset.

This data was sourced from [Baseball Savant](https://baseballsavant.mlb.com/), an MLB-owned platform, and cleaned and stored in a csv. The use of this data is for non-commercial and educational purposes only.

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
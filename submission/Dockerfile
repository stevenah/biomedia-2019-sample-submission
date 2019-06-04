
# Use an intermidate Docker image as base for our submissioin.
# Replace this with whatever is appropriate for your submission.
FROM gw000/keras:latest

# Install required pip packages
RUN pip install pillow

# Copy the contents of this directory (submission_1) 
# to the /submission path of the Docker image.
ADD . /submission

# Run the "submission_1.py" python file.
# For your submission, replace with your test script.
CMD [ "python", "/submission/submission_1.py" ]
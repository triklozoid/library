from python:3

COPY . /app
WORKDIR /app

RUN pip install pipenv

RUN pipenv install --system --deploy
RUN python manage.py collectstatic

# CMD ['python', "manage.py" "runserver"]
# CMD ["sh", "-c", "python manage.py runserver"]
#ENTRYPOINT ["pipenv", "run"]

ENTRYPOINT ["python", "manage.py"]
CMD ["runserver", "0.0.0.0:8000"]

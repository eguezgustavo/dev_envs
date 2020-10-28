# Docker image to run java/maven apps
Steps to activate it:

1. Build the image
```
docker build -t java-maven .
```

2. Run the image
```
docker run -d --name java-maven-sandbox java-maven
```

3. Open a terminal in the java/maven sandbox
```
docker exec -it java-maven-sandbox zsh
```

4. Clone the repository
```
cd code
git clone <repo-to-clone>
```

5. Open the code in visual studio code

Please follow [these](https://code.visualstudio.com/docs/remote/containers) instructions
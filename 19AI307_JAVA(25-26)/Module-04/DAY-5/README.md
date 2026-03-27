# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:

To implement the Memento Design Pattern in Java where an Article saves its content history and allows restoring any previous version.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Memento class to store the state (article content).
4. Create an Article class with methods to save and restore content using mementos.
5. Store all versions in a list and allow the user to select a version to restore.
6. Display the restored content and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by:  bala murugan s
RegisterNumber:212223230027
*/
```

## SOURCE CODE:


```py
import java.util.*;

class Article {
    private String content;

    public void setContent(String content) {
        this.content = content;
    }

    public String getContent() {
        return this.content;
    }

    public ArticleMemento save() {
        return new ArticleMemento(this.content);
    }

    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}

class ArticleMemento {
    private final String content;

    public ArticleMemento(String content) {
        this.content = content;
    }

    public String getContent() {
        return this.content;
    }
}

class ArticleHistory {
    private final List<ArticleMemento> versions = new ArrayList<>();

    public void saveVersion(Article article) {
        versions.add(article.save());
    }

    public ArticleMemento getVersion(int index) {
        if (index < 0 || index >= versions.size()) return null;
        return versions.get(index);
    }

    public int size() {
        return versions.size();
    }
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        if (!sc.hasNextInt()) {
            sc.close();
            return;
        }
        int n = sc.nextInt();
        sc.nextLine();
        Article article = new Article();
        ArticleHistory history = new ArticleHistory();
        for (int i = 0; i < n; i++) {
            if (!sc.hasNextLine()) break;
            String line = sc.nextLine();
            article.setContent(line);
            history.saveVersion(article);
        }
        if (!sc.hasNextInt()) {
            sc.close();
            return;
        }
        int restoreIndex = sc.nextInt();
        ArticleMemento m = history.getVersion(restoreIndex);
        if (m != null) {
            article.restore(m);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }
        sc.close();
    }
}
```

## OUTPUT:

<img width="986" height="368" alt="image" src="https://github.com/user-attachments/assets/1e640bd6-0797-45c2-9b96-60c9fa00e1a3" />


## RESULT:

Thus the program has been implemented and executed successfully.

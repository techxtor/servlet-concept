Servlet Concept
---
### Introduction:


### Working:
- To make a class as Servlet, make it a sub class of `javax.servlet.http.HttpServlet`
---
    public class HomeServlet extends HttpServlet {}
---

- In `web/WEB-INF/web.xml`, add `servlet` and `servlet-mapping` tags
    - `servlet/servlet-name` is the servlet name
    - `servlet/servlet-class` is the class associated with servlet name
    - `servlet-mapping/servlet`-name is the servlet name
    - `servlet-mapping/url-pattern` is the route pattern match
---
    <servlet>
        <servlet-name>add</servlet-name>
        <servlet-class>com.techxtor.servlets.AdderServlet</servlet-class>
    </servlet>
    <servlet-mapping>
        <servlet-name>add</servlet-name>
        <url-pattern>/add</url-pattern>
    </servlet-mapping>
---

- Override `service` method of `HttpServlet` class that takes `HttpServletRequest`, `HttpServletResponse` as parameters.
---
    @Override
    public void service(HttpServletRequest req, HttpServletResponse res) {}
---
- It is generic and accepts all http methods.
- request parameters can be accessed using `req.getParameter("__parameter-name__")`
- To send output, create object of `PrintWriter` class and print the content
---
    PrintWriter out = res.getWriter();
    out.println("___content__");
---

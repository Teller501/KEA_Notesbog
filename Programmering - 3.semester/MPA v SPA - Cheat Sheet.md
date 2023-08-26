# Multi-Page Application (MPA) Cheat Sheet

- **Definition**: Web app that loads multiple HTML pages as user navigates

- **Pages**: Each page is separate and requires full page refresh 

- **Examples**: Amazon, New York Times, Wikipedia  

- **Lifecycle**:
    - Browser requests page → Server returns HTML page → Browser renders page 
    - User clicks link → New request to server → Server returns new page → Browser renders new page

- **Pros**:
    - Good for SEO (unique URLs)
    - Secure (separate requests per page)
    - Fast initial load
    - Compatible with old browsers

- **Cons**:
    - Slower performance (full page refreshes)
    - More complex development (multiple pages) 
    - Higher server load (more requests)

# Single Page Application (SPA) Cheat Sheet

- **Definition**: Web app that loads single HTML page, updates content dynamically

- **Pages**: Single page loaded initially, additional views generated dynamically in browser

- **Examples**: Google Maps, Gmail, Facebook

- **Lifecycle**:
    - Browser requests page → Server returns initial HTML, JS
    - Browser renders page → User interacts → JS updates page via API calls 
    - No full page refresh

- **Pros**:
    - Faster after initial load 
    - Great user experience
    - Easier to maintain
    - Works offline
    - Reduced server load

- **Cons**:
    - Slower initial load    
    - SEO challenges
    - Browser compatibility issues
    - Potential security risks

- **Choosing**: Consider complexity, performance, SEO needs, time to market 

- **Deployment**: SPAs use static and API servers, MPAs use server-side rendering

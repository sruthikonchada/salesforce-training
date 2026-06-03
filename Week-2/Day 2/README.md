# LWC Communication

## Component Communication

Lightning Web Components communicate through different mechanisms based on component relationships.

- Parent to Child communication using `@api`
- Child to Parent communication using Custom Events
- Reusable and modular component architecture
- Efficient data sharing between components

---

## Dashboard Design

The dashboard is built using Lightning Web Components with a clean and responsive layout.

### Features
- User-friendly interface
- Reusable components
- Dynamic data display
- SLDS-based design

---

## Data Flow Explanation

The application follows a structured data flow:

1. Parent component passes data to child components using `@api`.
2. Child components handle user interactions.
3. Custom events are dispatched from child components.
4. Parent components receive events and update data accordingly.

This ensures better maintainability and predictable component behavior.

---

## Aura vs LWC

| Feature | Aura | LWC |
|----------|------|------|
| Performance | Good | Faster |
| Framework | Salesforce Specific | Web Standards Based |
| Complexity | Higher | Lower |
| Reusability | Supported | Highly Reusable |
| Developer Experience | Moderate | Better |

LWC is preferred for modern Salesforce development due to its performance and simplicity.

---

## Reflection

This exercise helped me understand component communication in Lightning Web Components. I learned how data flows between components using `@api` properties and custom events. It also improved my understanding of reusable component design and modern Salesforce development practices.
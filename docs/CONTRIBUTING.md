# Contributing to Business Simulator

## Code of Conduct

Be respectful, inclusive, and constructive in all interactions.

## Getting Started

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Make changes following our style guide
4. Commit with clear messages: `git commit -m "Add feature description"`
5. Push to your fork: `git push origin feature/your-feature`
6. Submit a Pull Request

## Development Setup

```bash
git clone https://github.com/YOUR-USERNAME/Business-Simulator.git
cd Business-Simulator
npm install
cp .env.example .env
# Configure .env with your database
mysql -u root -p < db/schema.sql
npm run dev
```

## Coding Standards

### JavaScript
- Use ES6+ syntax
- Follow existing code style
- Use meaningful variable names
- Add comments for complex logic
- Maximum line length: 100 characters

### Example
```javascript
// Good
const calculateProfit = (revenue, expenses) => {
  return revenue - expenses;
};

// Avoid
const cp=(r,e)=>r-e;
```

### Database
- Use prepared statements (prevent SQL injection)
- Add indexes for frequently queried columns
- Document schema changes

```javascript
// Good
const [users] = await connection.query(
  'SELECT * FROM users WHERE id = ?',
  [userId]
);

// Avoid
const users = await connection.query(
  `SELECT * FROM users WHERE id = ${userId}`
);
```

## API Development

### Endpoint Naming
- Use RESTful conventions
- Use plural nouns: `/api/businesses` not `/api/business`
- Use lowercase: `/api/businesses` not `/api/Businesses`

### Request/Response Format
```javascript
// Request
POST /api/businesses
{
  "name": "string",
  "type": "string",
  ...
}

// Response (Success)
{
  "message": "Description",
  "data": {...}
}

// Response (Error)
{
  "error": "Error description",
  "status": 400
}
```

## Frontend Development

### jQuery UI Integration
- Use jQuery UI widgets for dialogs, tabs, etc.
- Keep selectors simple and maintainable
- Use event delegation for dynamic elements

```javascript
// Good
$('#form').on('submit', function(e) {
  e.preventDefault();
  // handle form
});

// Avoid
$('#form').submit(function() { ... });
```

## Git Workflow

### Commit Messages
- Be descriptive: "Add user authentication" not "Fix stuff"
- Start with verb: "Add", "Fix", "Update", "Refactor"
- Reference issues: "Fix #123" closes issue 123

## Testing

```bash
npm test
```

## Questions?

Create an issue or start a discussion in the GitHub Discussions section.

Thank you for contributing! 🎉

# Contributing to IntelliCompliance

We welcome contributions to IntelliCompliance! This document provides guidelines for contributing to this project.

## 🚀 Quick Start

1. **Fork the repository**
2. **Clone your fork**
   ```bash
   git clone https://github.com/your-username/IntelliCompliance.git
   cd IntelliCompliance
   ```
3. **Install dependencies**
   ```bash
   npm install
   ```
4. **Start development server**
   ```bash
   node server.js
   ```

## 📋 Development Setup

### Prerequisites
- Node.js 12+ (tested with v12.22.12)
- npm or yarn
- Git

### Environment Setup
```bash
# Clone the repository
git clone https://github.com/your-username/IntelliCompliance.git
cd IntelliCompliance

# Install dependencies
npm install

# Start the server
node server.js
```

## 🔧 Code Style

### JavaScript Standards
- Use ES6+ features where appropriate
- Follow Node.js best practices
- Use meaningful variable names
- Add comments for complex logic

### File Structure
```
IntelliCompliance/
├── server.js              # Main server file
├── package.json           # Dependencies
├── README.md             # Documentation
├── data/                 # Data storage
├── logs/                 # Application logs
└── node_modules/         # Dependencies
```

## 🧪 Testing

### Running Tests
```bash
# Test server health
curl http://localhost:3000/api/health

# Test search functionality
curl "http://localhost:3000/api/search?q=test"
```

### Adding New Tests
- Add test cases for new features
- Ensure all endpoints return proper responses
- Test error handling

## 📝 Commit Guidelines

### Commit Message Format
```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

### Types
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes
- `refactor`: Code refactoring
- `test`: Adding tests
- `chore`: Maintenance tasks

### Examples
```
feat(api): add new search endpoint
fix(server): resolve data loading issue
docs(readme): update installation instructions
```

## 🔍 Pull Request Process

1. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes**
   - Write clean, documented code
   - Test your changes thoroughly
   - Update documentation if needed

3. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: add your feature description"
   ```

4. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

5. **Create a Pull Request**
   - Use a clear title and description
   - Reference any related issues
   - Include screenshots if applicable

## 🐛 Bug Reports

### Before Reporting
- Check existing issues
- Test with the latest version
- Gather relevant information

### Bug Report Template
```markdown
**Bug Description**
A clear description of the bug.

**Steps to Reproduce**
1. Go to '...'
2. Click on '....'
3. Scroll down to '....'
4. See error

**Expected Behavior**
What you expected to happen.

**Screenshots**
If applicable, add screenshots.

**Environment**
- OS: [e.g. macOS, Windows, Linux]
- Node.js version: [e.g. v12.22.12]
- Browser: [e.g. Chrome, Firefox]
```

## 💡 Feature Requests

### Feature Request Template
```markdown
**Feature Description**
A clear description of the feature.

**Use Case**
Why is this feature needed?

**Proposed Solution**
How should this feature work?

**Alternatives**
Other solutions you've considered.
```

## 🌍 Adding New Jurisdictions

### Data Collector Template
```javascript
async function collectNewJurisdiction() {
    try {
        // Implement data collection logic
        const data = await fetchFromAPI();
        return processData(data);
    } catch (error) {
        console.error('Error collecting data:', error);
        return [];
    }
}
```

### Steps to Add
1. Create data collector function
2. Add to jurisdiction list
3. Update documentation
4. Test thoroughly

## 📊 Performance Guidelines

### Best Practices
- Use efficient algorithms
- Minimize API calls
- Implement caching where appropriate
- Monitor memory usage

### Performance Testing
```bash
# Test server performance
curl -w "@curl-format.txt" -o /dev/null -s http://localhost:3000/api/search?q=test
```

## 🔒 Security Considerations

### Security Checklist
- [ ] Validate all inputs
- [ ] Sanitize data before processing
- [ ] Use HTTPS in production
- [ ] Implement rate limiting
- [ ] Keep dependencies updated

## 📖 Documentation

### Documentation Standards
- Use clear, concise language
- Include code examples
- Update README.md for major changes
- Add inline comments for complex logic

### API Documentation
- Document all endpoints
- Include request/response examples
- Specify error codes
- Add authentication requirements

## 🤝 Community Guidelines

### Code of Conduct
- Be respectful and inclusive
- Help others learn and grow
- Focus on constructive feedback
- Maintain professional communication

### Getting Help
- Check existing documentation
- Search closed issues
- Ask specific questions
- Provide context and examples

## 📞 Contact

For questions or support:
- Create an issue on GitHub
- Check the documentation
- Review existing discussions

## 📄 License

By contributing, you agree that your contributions will be licensed under the same license as the project.

---

Thank you for contributing to IntelliCompliance! 🎉 
# Contributing Guide

Thank you for your interest in improving this AI entrepreneur portfolio! While this is primarily a personal portfolio project, contributions and suggestions are welcome.

## Development Setup

### Prerequisites
- Node.js 18 or higher
- PostgreSQL database
- Git

### Local Development

1. **Fork the repository**
   ```bash
   git clone https://github.com/yourusername/asim-shaikh-ai-portfolio.git
   cd asim-shaikh-ai-portfolio
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment**
   ```bash
   cp .env.example .env
   # Edit .env with your database URL
   ```

4. **Start development server**
   ```bash
   npm run dev
   ```

## Code Style

### TypeScript
- Use TypeScript for all new code
- Follow existing type definitions
- Add proper type annotations

### React Components
- Use functional components with hooks
- Follow existing component structure
- Use Shadcn/ui components when possible

### Styling
- Use Tailwind CSS classes
- Follow existing design patterns
- Maintain dark theme consistency
- Keep 3D effects and animations smooth

### File Organization
```
client/src/
├── components/
│   ├── sections/     # Page sections
│   └── ui/          # Reusable components
├── hooks/           # Custom hooks
├── lib/             # Utilities
└── pages/           # Page components
```

## Making Changes

### Frontend Changes
- Components should be responsive
- Maintain accessibility standards
- Test animations and interactions
- Follow existing naming conventions

### Backend Changes
- Use TypeScript interfaces
- Follow REST API conventions
- Add proper error handling
- Update storage interface if needed

### Database Changes
- Use Drizzle ORM for schema changes
- Add migration scripts
- Update shared types in `shared/schema.ts`

## Testing

### Manual Testing
- Test all form submissions
- Verify responsive design
- Check animations and transitions
- Test in multiple browsers

### Before Submitting
- Run type checking: `npm run check`
- Test build process: `npm run build`
- Verify production build: `npm start`

## Pull Request Process

1. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes**
   - Follow code style guidelines
   - Add appropriate documentation
   - Test thoroughly

3. **Commit your changes**
   ```bash
   git commit -m "Add: brief description of changes"
   ```

4. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

5. **Create a Pull Request**
   - Describe your changes clearly
   - Include screenshots if UI changes
   - Reference any related issues

## Areas for Contribution

### Enhancements
- Performance optimizations
- Accessibility improvements
- New animation effects
- Mobile experience enhancements

### Bug Fixes
- Cross-browser compatibility
- Mobile responsiveness issues
- Animation glitches
- Form validation improvements

### Documentation
- Code comments
- README improvements
- Deployment guides
- API documentation

## Code Review

### What We Look For
- Code quality and readability
- Performance considerations
- Accessibility compliance
- Mobile responsiveness
- TypeScript best practices

### Review Process
1. Automated checks (TypeScript, build)
2. Manual code review
3. Testing verification
4. Deployment compatibility

## Communication

### Issues
- Use GitHub Issues for bug reports
- Provide detailed reproduction steps
- Include browser and device information
- Add screenshots when helpful

### Suggestions
- Open an issue for feature requests
- Describe the problem you're solving
- Provide context and use cases
- Consider implementation complexity

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

## Questions?

If you have questions about contributing:
1. Check existing issues and discussions
2. Review the README.md file
3. Open a new issue with the "question" label

Thank you for helping make this portfolio better! 🚀

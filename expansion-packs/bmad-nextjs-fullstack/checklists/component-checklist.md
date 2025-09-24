# React Component Development Checklist

## Pre-Development
- [ ] Component purpose and requirements clearly defined
- [ ] Component interface (props) designed
- [ ] Accessibility requirements identified
- [ ] Design mockup/wireframe available

## Development
- [ ] TypeScript interface defined for all props
- [ ] Component follows naming conventions (PascalCase)
- [ ] Proper file structure and organization
- [ ] Default props defined where appropriate
- [ ] Error boundaries implemented for critical components

## Styling
- [ ] Tailwind CSS classes used consistently
- [ ] Responsive design implemented
- [ ] Dark mode support (if applicable)
- [ ] Custom CSS kept to minimum
- [ ] CSS class conflicts avoided

## Accessibility (a11y)
- [ ] Semantic HTML elements used
- [ ] ARIA labels added where needed
- [ ] Keyboard navigation supported
- [ ] Focus management implemented
- [ ] Screen reader friendly
- [ ] Color contrast meets WCAG guidelines

## Performance
- [ ] Unnecessary re-renders avoided
- [ ] React.memo used where appropriate
- [ ] Heavy computations memoized with useMemo
- [ ] Event handlers memoized with useCallback
- [ ] Large lists virtualized (if applicable)

## Testing
- [ ] Unit tests written and passing
- [ ] Component renders without crashing
- [ ] Props validation tested
- [ ] User interactions tested
- [ ] Edge cases covered
- [ ] Accessibility testing performed

## Code Quality
- [ ] TypeScript types are strict and accurate
- [ ] ESLint rules pass
- [ ] Prettier formatting applied
- [ ] No console errors or warnings
- [ ] Code is self-documenting
- [ ] Comments added for complex logic

## Integration
- [ ] Component integrates well with parent components
- [ ] State management working correctly
- [ ] API calls handled properly (if applicable)
- [ ] Error states handled gracefully
- [ ] Loading states implemented

## Documentation
- [ ] Component documented with JSDoc comments
- [ ] Props interface documented
- [ ] Usage examples provided
- [ ] Storybook story created (if using Storybook)

## Review
- [ ] Code review completed
- [ ] Design review completed
- [ ] Performance review completed
- [ ] Accessibility review completed
- [ ] Security review completed (if handling sensitive data)
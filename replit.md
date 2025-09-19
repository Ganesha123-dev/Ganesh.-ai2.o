# Ganesh A.I. - AI-Powered Money-Making Platform

## Overview

Ganesh A.I. is a comprehensive AI-powered platform that combines multiple AI models (GPT-4, Claude, Gemini) with a monetization system allowing users to earn money through AI interactions. The platform features a modern web application with ChatGPT-like interface, integrated Telegram bot, comprehensive admin panel, and multiple payment gateway integrations. The system is designed for production deployment with real-time analytics, user management, and revenue generation capabilities.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Modern Web Interface**: Bootstrap 5-based responsive design with ChatGPT-like chat interface
- **Real-time Chat System**: JavaScript-powered instant messaging with typing indicators and error handling
- **Multi-device Support**: Mobile-responsive design optimized for all screen sizes
- **Progressive Enhancement**: Fallback systems for degraded network conditions

### Backend Architecture
- **Flask Web Framework**: Python-based web application with modular route structure
- **SQLAlchemy ORM**: Database abstraction layer supporting SQLite for development and PostgreSQL for production
- **RESTful API Design**: JSON-based API endpoints for frontend communication and external integrations
- **Session Management**: Secure user authentication with password hashing and session tokens
- **Background Job Processing**: APScheduler for handling periodic tasks and analytics updates

### Data Storage Solutions
- **Primary Database**: SQLite for development, configurable for PostgreSQL in production
- **User Management**: Comprehensive user profiles with wallet balances, referral tracking, and activity logs
- **Transaction Logging**: Complete audit trail for all financial transactions and AI usage
- **Analytics Storage**: Real-time metrics storage for user activity, earnings, and system performance

### Authentication and Authorization
- **Role-based Access Control**: Admin and regular user roles with different permission levels
- **Secure Password Handling**: Werkzeug-based password hashing with salt
- **Session Security**: Flask session management with configurable secret keys
- **Admin Panel Protection**: Separate authentication flow for administrative functions

### AI Integration Architecture
- **Multi-Model Support**: Primary OpenAI GPT integration with HuggingFace fallback
- **Cost Management**: Per-request pricing with different rates for free and premium models
- **Error Handling**: Automatic fallback between AI providers for reliability
- **Response Caching**: Intelligent caching to reduce API costs and improve response times

### Monetization System
- **Earning Mechanisms**: Visit-based earnings (₹0.001 per visit), chat earnings (₹0.05 per message), referral bonuses (₹10 per referral)
- **Premium Subscriptions**: Monthly (₹99) and yearly (₹999) plans with enhanced features
- **Wallet System**: Real-time balance tracking with transaction history
- **Withdrawal Processing**: Automated payout system with configurable thresholds

## External Dependencies

### AI Services
- **OpenAI API**: Primary AI model provider (GPT-4, GPT-3.5-turbo) with configurable model selection
- **HuggingFace API**: Fallback AI service for reliability and cost optimization
- **Custom AI Responses**: Fallback response system for offline scenarios

### Payment Gateways
- **Cashfree**: Indian payment gateway with order creation, verification, and webhook handling
- **PayPal**: International payments with sandbox and production environment support
- **Stripe**: Credit card processing with subscription management capabilities
- **Razorpay**: Additional Indian payment gateway for redundancy

### Communication Services
- **Telegram Bot API**: Real-time bot integration with webhook support for instant messaging
- **Email Services**: SMTP integration for user notifications and account management
- **SMS Integration**: Optional SMS verification and notifications

### Infrastructure Services
- **Render**: Primary deployment platform with automatic scaling
- **PostgreSQL**: Production database service
- **Redis**: Session storage and caching (configurable)
- **CDN Services**: Static asset delivery optimization

### Monitoring and Analytics
- **APScheduler**: Background job processing for analytics and maintenance tasks
- **Custom Logging**: Comprehensive logging system with file and console outputs
- **Health Monitoring**: Automatic system health checks and error reporting
- **Usage Analytics**: Real-time tracking of user activity and system performance

### Security and Compliance
- **HTTPS Enforcement**: SSL/TLS encryption for all communications
- **CSRF Protection**: Built-in Flask security features
- **Input Validation**: Comprehensive sanitization of user inputs
- **Rate Limiting**: API request throttling to prevent abuse
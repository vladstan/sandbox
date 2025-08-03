# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a simple HTML5 starter template designed for deployment on Vercel. The project consists of a single-page application with integrated analytics, security headers, and edge middleware.

## Key Files

- `index.html` - Main HTML page with Vercel Analytics integration
- `middleware.js` - Vercel Edge Middleware for security headers
- `package.json` - Contains only @vercel/edge dependency (no build scripts)

## Architecture

The project uses Vercel Edge Middleware to add security headers to all requests. The middleware function in `middleware.js` sets:
- Referrer Policy
- X-Frame-Options (DENY)
- X-Content-Type-Options (nosniff)
- X-DNS-Prefetch-Control
- Strict-Transport-Security

## Development

This is a static HTML project with no build process. Changes can be made directly to:
- `index.html` for content updates
- `middleware.js` for routing/security header modifications

## Deployment

The project is configured for Vercel deployment with:
- Automatic git integration
- Edge Network distribution
- Built-in gzip compression
- Vercel Analytics via script tag

No build, test, or lint commands are configured as this is a simple static HTML template.
<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Package -  AdminLTE integration with Laravel

This package provides an easy way to quickly set up AdminLTE v3 with Laravel (7 or higher). It has no others requirements and dependencies besides Laravel, so you can start building your admin panel immediately. The package provides a blade template that you can extend and an advanced menu configuration system. Also, and optionally, the package offers a set of AdminLTE styled authentication views that you can use in replacement of the ones that are provided by the legacy laravel/ui authentication scaffolding.

1. Require the package

```
composer require jeroennoten/laravel-adminlte
```

2. Install the package resources
```
php artisan adminlte:install
```

3. Install the legacy authentication scaffolding 

```
composer require laravel/ui
php artisan ui bootstrap --auth
```

```
php artisan adminlte:install --only=auth_views
```

### Usage
- Dashboard page

```
@extends('adminlte::page')

@section('title', 'Dashboard')

@section('content_header')
    <h1>Dashboard</h1>
@stop

@section('content')
    <p>Welcome to this beautiful admin panel.</p>
@stop

@section('css')
    {{-- Add here extra stylesheets --}}
    {{-- <link rel="stylesheet" href="/css/admin_custom.css"> --}}
@stop

@section('js')
    <script> console.log("Hi, I'm using the Laravel-AdminLTE package!"); </script>
@stop
```